> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Vercel - Upstash Redis Integration

If you are using [Vercel](https://vercel.com/) then you can integrate Upstash
Redis, Vector, Search or QStash to your project easily. Upstash is the perfect serverless
solution for your applications thanks to its:

* Low latency data
* Per request pricing
* Durable storage
* Ease of use

Below are the steps of the integration.

## Add Integration to Your Vercel Account

Visit the [Upstash Integration](https://vercel.com/integrations/upstash) on
Vercel and click the `Install` button. If you are installing an Upstash integration
for the first time, you will be prompted to choosing between connecting an existing Upstash
account or letting Vercel manage an Upstash account for you.

<img src="https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/vercel_integration_create.png?fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=7ddb17b7704d1783fd33fbec684d382f" width="520" data-og-width="1210" data-og-height="657" data-path="img/vercel/vercel_integration_create.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/vercel_integration_create.png?w=280&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=e2ab149cff9d2bfbac828e5fb65ffd27 280w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/vercel_integration_create.png?w=560&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=f4fb69577ae86807900e89d5ee29e103 560w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/vercel_integration_create.png?w=840&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=0d142acab3fdc121b8c6314229122638 840w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/vercel_integration_create.png?w=1100&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=213c9ecd06073b85ed7de8bc4c84a395 1100w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/vercel_integration_create.png?w=1650&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=aa0791adaa501f32d932d12848769456 1650w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/vercel_integration_create.png?w=2500&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=217ea8a4bfeb010faa10bfc926f03a58 2500w" />

In both cases, you will be able to create and use a redis database as usual. If you let Vercel
manage your Upstash account, you can handle payments, database creation and deletion directly from the Vercel dashboard.

If you choose to connect an existing Upstash account, you will be able to utilize features on Upstash Console
such as teams and audit logs.

### Option 1: "Create New Upstash Account"

If you choose this option, Vercel will prompt you to choose one of the products available on Upstash,
configure the database (by choosing database name, regions, plan). After you finish the configuration,
Vercel will create the Upstash account and the selected resources for you and redirect you to the
page of the created resource on Vercel dashboard.

On the Vercel dashboard, you will be able to find the credentials of the database, change the database
name, update the regions or plan.

<img src="https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/vercel_dashboard.png?fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=146cab752ab283c660ca333bdc18ca14" width="520" data-og-width="1210" data-og-height="665" data-path="img/vercel/vercel_dashboard.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/vercel_dashboard.png?w=280&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=4429f37ff266f8826dda35e2506d8d4e 280w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/vercel_dashboard.png?w=560&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=39ff2bdf5c087b418ed4065dfced07d6 560w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/vercel_dashboard.png?w=840&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=bebcb6ee873323e16796088a0dd6fb69 840w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/vercel_dashboard.png?w=1100&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=6d18e6ca0fd8221d001bd266d1b1c3f1 1100w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/vercel_dashboard.png?w=1650&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=fb00f1f4bf1a100578f3f291619b4a3e 1650w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/vercel_dashboard.png?w=2500&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=b78a544f6c7054240b612bd484675c45 2500w" />

You can also go to the `Settings` tab and connect your apps on Vercel to the database, making the credentials
of the database available to the app as environment variables.

### Option 2: "Link Existing Upstash Account"

Vercel will redirect you to Upstash, where you can select your Vercel project
and Upstash resources that you want to integrate.

<Tip>
  You should login to [the Upstash Console](https://console.upstash.com/) with your account if you
  are not logged in before clicking continue.
</Tip>

<Frame>
  <img src="https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/integration_init.png?fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=3ba54cc2387ad309508e0ce02609a2f5" width="520" data-og-width="732" data-og-height="607" data-path="img/vercel/integration_init.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/integration_init.png?w=280&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=8f9cdd777c0cf0045344552951d2046e 280w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/integration_init.png?w=560&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=70a7d04d31aaea1d00c36b59a46e17ff 560w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/integration_init.png?w=840&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=66f324ba3bc8291fc00e915d8610913e 840w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/integration_init.png?w=1100&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=7083c6ebd83b23e3489431dce34c9ecc 1100w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/integration_init.png?w=1650&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=518c13808bf283fb5babe404d4c107a4 1650w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/integration_init.png?w=2500&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=167383774a2bcae7444818fe8cab5144 2500w" />
</Frame>

If you do not have a Redis database yet, you can create one
from the dropdown menu.

<Frame>
  <img src="https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/integration_redis_create.png?fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=4ed4dde36532aa6dafdf6e73a920617e" width="520" data-og-width="732" data-og-height="627" data-path="img/vercel/integration_redis_create.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/integration_redis_create.png?w=280&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=99e105f480bbdf2504fae32d0665c945 280w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/integration_redis_create.png?w=560&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=2c9e066e78f912ef8c349474372e6e24 560w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/integration_redis_create.png?w=840&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=273b3a8ea22b3fb794fb6ff6b4500251 840w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/integration_redis_create.png?w=1100&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=d3cd2ae4d253e56a452ba41deefb03bb 1100w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/integration_redis_create.png?w=1650&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=d3df90bfad7c6877c8e67a4622498741 1650w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/integration_redis_create.png?w=2500&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=4da2d68f1913703c0fcef731aaab24d9 2500w" />
</Frame>

Once you have selected all resources, click the `Save` button at the bottom of
the page.

After all environment variables are created, you will be forwarded to Vercel. Go
to your project settings where you can see all added environment variables.

<Tip>
  You need to redeploy your app for the environment variable to be used.
</Tip>

The [Integration Dashboard](https://console.upstash.com/integration/vercel)
allows you to see all your integrations, link new projects or manage existing
ones.

<Frame>
  <img src="https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/integration_dashboard.png?fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=9d0f827ee454d30d24636740f83dd30b" data-og-width="1199" width="1199" data-og-height="618" height="618" data-path="img/vercel/integration_dashboard.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/integration_dashboard.png?w=280&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=1743bcd4c549a4a3909273b3f9c95145 280w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/integration_dashboard.png?w=560&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=01e67d7ed31aa99999444d7a9c90c363 560w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/integration_dashboard.png?w=840&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=a9321fd78b137b5b17db53b690837d07 840w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/integration_dashboard.png?w=1100&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=cfcd45cf4a0ef149edabb801bc19c83f 1100w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/integration_dashboard.png?w=1650&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=37d2592873d4ca91531faedf7ebc47d3 1650w, https://mintcdn.com/upstash/jORuCV5FkbdVFZ31/img/vercel/integration_dashboard.png?w=2500&fit=max&auto=format&n=jORuCV5FkbdVFZ31&q=85&s=0842fcb83d911aac2e156275fe8fdc39 2500w" />
</Frame>

## Use Upstash in Your App

If you completed the integration steps above and redeploy your app, the added
environment variables will be accessible inside your Vercel application. You can
now use them in your clients to connect

### Redis

```ts  theme={"system"}
import { Redis } from "@upstash/redis";
import { type NextRequest, NextResponse } from "next/server";

const redis = Redis.fromEnv();

export const POST = async (request: NextRequest) => {
  await redis.set("foo", "bar");
  const bar = await redis.get("foo");
  return NextResponse.json({
    body: `foo: ${bar}`,
  });
}
```

### QStash

**Client**

```ts  theme={"system"}
import { Client } from "@upstash/qstash";

const client = new Client({
  token: process.env.QSTASH_TOKEN,
});

const res = await client.publishJSON({
  url: "https://my-api...",
  body: {
    hello: "world",
  },
});
```

**Receiver**

```ts  theme={"system"}
import { Receiver } from "@upstash/qstash";

const receiver = new Receiver({
  currentSigningKey: process.env.QSTASH_CURRENT_SIGNING_KEY,
  nextSigningKey: process.env.QSTASH_NEXT_SIGNING_KEY,
});

const isValid = await receiver.verify({
  signature: "..."
  body: "..."
})
```

### Vector

```ts  theme={"system"}
import { Index } from "@upstash/vector";

const index = new Index({
  url: process.env.UPSTASH_VECTOR_REST_URL,
  token: process.env.UPSTASH_VECTOR_REST_TOKEN,
});

await index.upsert({
  id: "1",
  data: "Hello world!",
  metadata: { "category": "greeting" }
})
```

### Search

```ts  theme={"system"}
import { Search } from "@upstash/search";

const client = new Search({
  url: process.env.UPSTASH_SEARCH_REST_URL,
  token: process.env.UPSTASH_SEARCH_REST_TOKEN,
});

const index = client.index("my-index");
await index.upsert({
  id: "1",
  content: { text: "Hello world!" },
  metadata: { category: "greeting" }
});
```

## Support

If you have any issue you can ask in our
[Discord server](https://discord.gg/w9SenAtbme) or send email at
[support@upstash.com](mailto:support@upstash.com)
