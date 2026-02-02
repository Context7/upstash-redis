> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Building a Serverless Notification API for Your Web Application with Redis

> This tutorial shows how to create a Serverless Notification API for Your Web Application with Redis.

Notifications and announcements help you communicate with your web site
visitors. It is not feasible to update your code and redeploy your website each
time you want to show a new message. It may also be too much investment to set
up a backend and maintain it to just serve these notifications. In this article,
we will build a website which will load the notification message directly from
the Redis database without a backend.

### Backendless? How is that possible?

Yes, we will not use any backend service, even a serverless function. We will
access Redis from the client side directly. This is possible with the read only
REST API provided by Upstash.

### Requirements

* The page will display a notification if the user has not already seen the
  notification before.
* The page will only show the latest notification.

Check out
[the code here](https://github.com/upstash/examples/tree/master/examples/serverless-notification-api).

### Project Setup

I will create a React application but you can use any other web framework. It
will simply call the Redis REST API and show the message as a notification.

Create the app:

```shell  theme={"system"}
npx create-react-app serverless-notification-api
```

Install a toast component to show the notification:

```shell  theme={"system"}
npm install --save react-toastify
```

Create a free database from [Upstash](https://console.upstash.com/) and copy the
REST url and read only token. You should switch the Read-Only Token setting. In
the database details page, click on the `Read-Only Token` switch.

<img src="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/restapi.png?fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=674b186c9592c05dd01faf66642b3691" alt="alt_text" data-og-width="1406" width="1406" data-og-height="230" height="230" data-path="img/examples/restapi.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/restapi.png?w=280&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=4b88fee1f50e2035eb17b886e9f660e2 280w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/restapi.png?w=560&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=e2770a511c8cd3ffd32289d82d7d5dcb 560w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/restapi.png?w=840&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=dc6bb0925816315aff765c2c4641c6b2 840w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/restapi.png?w=1100&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=c018b7aa446ef674b824bcb70096bcbc 1100w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/restapi.png?w=1650&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=f029092e5e0cd119f39d6711a5908a28 1650w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/restapi.png?w=2500&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=7881d4ab4683a475de136022c40fd8c0 2500w" />

### Implementation

The logic is simple. We will keep the notifications in a Redis Sorted Set. We
will keep a version (integer) in the local storage. We will use the versions as
scores in the sorted set. Each notification message will have a version (score)
and the higher score means the newer message. At each page load, we will query
the Redis sorted set to load the messages which have higher scores than the
locally stored version. After loading a notification message I will set my local
version equal to the latest notification’s version. This will prevent showing
the same notification to the same users more than once. Here the implementation:

```javascript  theme={"system"}
import logo from "./logo.svg";
import "./App.css";
import { toast, ToastContainer } from "react-toastify";
import "react-toastify/dist/ReactToastify.css";
import { useEffect } from "react";

function App() {
  useEffect(() => {
    async function fetchData() {
      try {
        let version = localStorage.getItem("notification-version");
        version = version ? version : 0;
        const response = await fetch(
          "REPLACE_UPSTASH_REDIS_REST_URL/zrevrangebyscore/messages/+inf/" +
            version +
            "/WITHSCORES/LIMIT/0/1",
          {
            headers: {
              Authorization: "Bearer REPLACE_UPSTASH_REDIS_REST_TOKEN",
            },
          }
        );
        const res = await response.json();
        const v = parseInt(res.result[1]);
        if (v) {
          localStorage.setItem("notification-version", v + 1);
        }
        toast(res.result[0]);
      } catch (e) {
        console.error(e);
      }
    }
    fetchData();
  });

  return (
    <div className="App">
      <header className="App-header">
        <img src={logo} className="App-logo" alt="logo" />
        <p>
          Edit <code>src/App.js</code> and save to reload.
        </p>
        <a
          className="App-link"
          href="https://reactjs.org"
          target="_blank"
          rel="noopener noreferrer"
        >
          Learn React
        </a>
      </header>
      <ToastContainer />
    </div>
  );
}

export default App;
```

### How to Add New Notification Messages

You can simply add new messages to the Redis sorted set with a highest score so
it will be displayed to the user with page loads. For our application the name
of the sorted set is `messages`.

<img src="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/notif/cli.png?fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=b67b4fc3620f906ffc0061f4be4fe005" alt="alt_text" data-og-width="1410" width="1410" data-og-height="142" height="142" data-path="img/examples/notif/cli.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/notif/cli.png?w=280&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=3cc5eae3334aafc58415c047e717b652 280w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/notif/cli.png?w=560&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=43e45fddbf765d41026fe7e2877dc8c8 560w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/notif/cli.png?w=840&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=b04310f0f2900df40dd3b7da2313ef9f 840w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/notif/cli.png?w=1100&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=9a54e968e0afec09d043e99e55098c05 1100w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/notif/cli.png?w=1650&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=fad2a15ebadd1a8088ed5075f4415948 1650w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/notif/cli.png?w=2500&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=5cf2945da1739cdb4ae616a3392ee37b 2500w" />

You can also remove a message using the [ZREM](https://redis.io/commands/zrem)
command.

### Conclusion

You do not need a backend to access Upstash Redis thanks to the REST API. You
can expose the token with your client side application, as the token only allows
read-only access. This helps developers to build applications without backend
for many use cases where the data is already available publicly.
