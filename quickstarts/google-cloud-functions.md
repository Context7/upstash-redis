> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Google Cloud Functions

<Card title="GitHub Repository" icon="github" href="https://github.com/upstash/redis-js/tree/main/examples/google-cloud-functions" horizontal>
  You can find the project source code on GitHub.
</Card>

### Prerequisites

1. [Create a Google Cloud Project.](https://cloud.google.com/resource-manager/docs/creating-managing-projects)
2. [Enable billing for your project.](https://cloud.google.com/billing/docs/how-to/verify-billing-enabled#console)
3. Enable Cloud Functions, Cloud Build, Artifact Registry, Cloud Run, Logging, and Pub/Sub APIs.

### Database Setup

Create a Redis database using [Upstash Console](https://console.upstash.com) or [Upstash CLI](https://github.com/upstash/cli). Copy `UPSTASH_REDIS_REST_URL` and `UPSTASH_REDIS_REST_TOKEN` for the next steps.

### Counter Function Setup & Deploy

1. Go to [Cloud Functions](https://console.cloud.google.com/functions/list) in Google Cloud Console.
2. Click **Create Function**.
3. Setup **Basics and Trigger** Configuration like below:
   <img src="https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-gcloud/basics.png?fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=007ed606059c1a85715b71f3cc93f7d8" alt="" data-og-width="1090" width="1090" data-og-height="1082" height="1082" data-path="img/redis-gcloud/basics.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-gcloud/basics.png?w=280&fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=43b1d3e50933c5dcfa82b66fc851a7a0 280w, https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-gcloud/basics.png?w=560&fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=7004784999274823be6d91f4fada8507 560w, https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-gcloud/basics.png?w=840&fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=f898ec6c37fe88ca6ea160cb5d6c128e 840w, https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-gcloud/basics.png?w=1100&fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=2871baf9499c25407ad19cf314871b28 1100w, https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-gcloud/basics.png?w=1650&fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=a3a3397a7490aaa2f81fde3081af7cdd 1650w, https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-gcloud/basics.png?w=2500&fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=3c6c312c51df82b43ae09ff00d414a81 2500w" />
4. Using your `UPSTASH_REDIS_REST_URL` and `UPSTASH_REDIS_REST_TOKEN`, setup **Runtime environment variables** under **Runtime, build, connections and privacy settings** like below.
   <img src="https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-gcloud/environment.png?fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=e23d98d5b0c2619d971719dac8899931" alt="" data-og-width="1006" width="1006" data-og-height="432" height="432" data-path="img/redis-gcloud/environment.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-gcloud/environment.png?w=280&fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=d1d4089e0dab97bd4f9c722792e3f665 280w, https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-gcloud/environment.png?w=560&fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=2f0f5f385024764675ac77ca35de41e9 560w, https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-gcloud/environment.png?w=840&fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=2ffe0b80e0a93ac3eceb060fa0ae8bb6 840w, https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-gcloud/environment.png?w=1100&fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=321957fba3db5bdc17b51bf3af983cef 1100w, https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-gcloud/environment.png?w=1650&fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=d2821b72c40318f56fabb809970bbe62 1650w, https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-gcloud/environment.png?w=2500&fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=af5fbdb53b54bb2953ec0c56a6454c44 2500w" />
5. Click **Next**.
6. Set **Entry point** to `counter`.
7. Update `index.js`

```js index.js theme={"system"}
const { Redis } = require("@upstash/redis");
const functions = require('@google-cloud/functions-framework');

const redis = new Redis({
  url: process.env.UPSTASH_REDIS_REST_URL,
  token: process.env.UPSTASH_REDIS_REST_TOKEN
});

functions.http('counter', async (req, res) => {
  const count = await redis.incr("counter");
  res.send("Counter:" + count);
});
```

8. Update `package.json` to include `@upstash/redis`.

```json package.json theme={"system"}
{
  "dependencies": {
    "@google-cloud/functions-framework": "^3.0.0",
    "@upstash/redis": "^1.31.6"
  }
}
```

9. Click **Deploy**.
10. Visit the given URL.
