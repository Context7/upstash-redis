> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Backendless Coin Price List with GraphQL API, Serverless Redis and Next.JS

In this tutorial, we will develop a simple coin price list using GraphQL API of
Upstash. You can call the application `backendless` because we will access the
database directly from the client (javascript). See the
[code](https://github.com/upstash/examples/tree/master/examples/coin-price-list).

<Frame>
  <img src="https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/coin-price-list/coin-price-list.png?fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=4cc171b213a162cdf7be374cb7fac8aa" width="800" data-og-width="978" data-og-height="838" data-path="img/coin-price-list/coin-price-list.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/coin-price-list/coin-price-list.png?w=280&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=1b11b6e6b6cfff8dd5ac4f6667729b0f 280w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/coin-price-list/coin-price-list.png?w=560&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=98661149f74b188766906b70c818594d 560w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/coin-price-list/coin-price-list.png?w=840&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=26ff2dd16d3b983ffd2232186b81663c 840w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/coin-price-list/coin-price-list.png?w=1100&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=5cf6db7c709559f0d3928c58a11b47cd 1100w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/coin-price-list/coin-price-list.png?w=1650&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=f41aab64d68ef20b3cca5ce108307435 1650w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/coin-price-list/coin-price-list.png?w=2500&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=d73c91b72d1e6c8058839c4dc7bf2f09 2500w" />
</Frame>

## Motivation

We want to give a use case where you can use the GraphQL API without any backend
code. The use case is publicly available read only data for web applications
where you need low latency. The data is updated frequently by another backend
application, you want your users to see the last updated data. Examples:
Leaderboards, news list, blog list, product list, top N items in the homepages.

### `1` Project Setup:

Create a Next application: `npx create-next-app`.

Install Apollo GraphQL client: `npm i @apollo/client`

### `2` Database Setup

If you do not have one, create a database following this
[guide](../overall/getstarted). Connect your database via Redis CLI and run:

```shell  theme={"system"}
rpush coins '{ "name" : "Bitcoin", "price": 56819, "image": "https://s2.coinmarketcap.com/static/img/coins/64x64/1.png"}' '{ "name" : "Ethereum", "price": 2130, "image": "https://s2.coinmarketcap.com/static/img/coins/64x64/1027.png"}' '{ "name" : "Cardano", "price": 1.2, "image": "https://s2.coinmarketcap.com/static/img/coins/64x64/2010.png"}' '{ "name" : "Polkadot", "price": 35.96, "image": "https://s2.coinmarketcap.com/static/img/coins/64x64/6636.png"}' '{ "name" : "Stellar", "price": 0.506, "image": "https://s2.coinmarketcap.com/static/img/coins/64x64/512.png"}'
```

### `3` Code

In the Upstash console, copy the read only access key in your API configuration
page (GraphQL Explorer > Configure API). In the `_app.js` create the Apollo
client and replace the your access key as below:

<Warning>
  You need to use Read Only Access Key, because the key will be accessible
  publicly.
</Warning>

```javascript  theme={"system"}
import "../styles/globals.css";
import {
  ApolloClient,
  ApolloProvider,
  createHttpLink,
  InMemoryCache,
} from "@apollo/client";

const link = createHttpLink({
  uri: "https://graphql-us-east-1.upstash.io/",
  headers: {
    Authorization: "Bearer YOUR_ACCESS_TOKEN",
  },
});
const client = new ApolloClient({
  uri: "https://graphql-us-east-1.upstash.io/",
  cache: new InMemoryCache(),
  link,
});

function MyApp({ Component, pageProps }) {
  return (
    <ApolloProvider client={client}>
      <Component {...pageProps} />{" "}
    </ApolloProvider>
  );
}

export default MyApp;
```

Edit `index.js` as below:

```javascript  theme={"system"}
import Head from "next/head";
import styles from "../styles/Home.module.css";
import { gql, useQuery } from "@apollo/client";
import React from "react";

const GET_COIN_LIST = gql`
  query {
    redisLRange(key: "coins", start: 0, stop: 6)
  }
`;

export default function Home() {
  let coins = [];
  const { loading, error, data } = useQuery(GET_COIN_LIST);

  if (!loading && !error) {
    for (let x of data.redisLRange) {
      let dd = JSON.parse(x);
      coins.push(dd);
    }
  }

  return (
    <div className={styles.container}>
      <Head>
        <title>Create Next App</title>
        <link rel="icon" href="/favicon.ico" />
      </Head>

      <main className={styles.main}>
        <h3 className={styles.title}>Coin Price List</h3>

        <div className={styles.grid}>
          <table className={styles.coins}>
            <tbody>
              {!loading ? (
                coins.map((item, ind) => (
                  <tr key={ind}>
                    <td>
                      <img src={item.image} width="25" />
                    </td>
                    <td>{item.name}</td>
                    <td className={styles.price}>${item.price}</td>
                  </tr>
                ))
              ) : (
                <tr>
                  <td>
                    <img src="/loader.gif" />
                  </td>
                </tr>
              )}
            </tbody>
          </table>
        </div>
      </main>

      <footer className={styles.footer}>
        <p className={styles.description}>
          <a href="https://docs.upstash.com"> Click for the tutorial </a>
        </p>
      </footer>
    </div>
  );
}
```

### `4` Run

Run your application locally: `npm run dev`

### `5` Live!

Go to [http://localhost:3000/](http://localhost:3000/) 🎉
