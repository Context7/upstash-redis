> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Deno Deploy

This is a step-by-step guide on how to use Upstash Redis to create a view
counter in your Deno deploy project.

### Create a database

Create a Redis database using [Upstash Console](https://console.upstash.com) or
[Upstash CLI](https://github.com/upstash/cli). Select the global to minimize the
latency from all edge locations. Copy the `UPSTASH_REDIS_REST_URL` and
`UPSTASH_REDIS_REST_TOKEN` for the next steps.

### Create a Deno deploy project

Go to [https://dash.deno.com/projects](https://dash.deno.com/projects) and
create a new playground project.

<img src="https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-deno/create.png?fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=6cb71bf83b9a0df25b5457e6efe3b500" alt="" data-og-width="2056" width="2056" data-og-height="1308" height="1308" data-path="img/redis-deno/create.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-deno/create.png?w=280&fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=2de9ae1edfca54b35d9eb159e59e38de 280w, https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-deno/create.png?w=560&fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=b5ef2baf9818d05d0480b7db02405566 560w, https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-deno/create.png?w=840&fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=ee6916085e844938a85477e1d470b811 840w, https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-deno/create.png?w=1100&fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=439b4d7d78a4300e13fdd43929d8fcaf 1100w, https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-deno/create.png?w=1650&fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=3d0f34898f283b2f5d94e7948effd09d 1650w, https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-deno/create.png?w=2500&fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=29fd67668409aa7d02ffe551861a6ff4 2500w" />

### 2. Edit the handler function

Then paste the following code into the browser editor:

```ts  theme={"system"}
import { serve } from "https://deno.land/std@0.142.0/http/server.ts";
import { Redis } from "https://deno.land/x/upstash_redis@v1.14.0/mod.ts";

serve(async (_req: Request) => {
  if (!_req.url.endsWith("favicon.ico")) {
    const redis = new Redis({
      url: "UPSTASH_REDIS_REST_URL",
      token: "UPSTASH_REDIS_REST_TOKEN",
    });

    const counter = await redis.incr("deno-counter");
    return new Response(JSON.stringify({ counter }), { status: 200 });
  }
});
```

### 3. Deploy and Run

Simply click on `Save & Deploy` at the top of the screen.

<img src="https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-deno/deploy.png?fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=9b2c12804600632014a6ca7303a9f72c" alt="" data-og-width="2962" width="2962" data-og-height="1492" height="1492" data-path="img/redis-deno/deploy.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-deno/deploy.png?w=280&fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=c9e4dbe9329b0b51b99fa30ad58a424c 280w, https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-deno/deploy.png?w=560&fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=cb6f0245fe154bc06c1d809f59529eac 560w, https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-deno/deploy.png?w=840&fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=4ac9892f2d8417eeed6a6a506b24c127 840w, https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-deno/deploy.png?w=1100&fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=aab0ddf63ead58d891eec12d37d8a9a7 1100w, https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-deno/deploy.png?w=1650&fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=3e12f7b42470a62802bc2cd354047cbc 1650w, https://mintcdn.com/upstash/fy-PVAyWJaRFn1UN/img/redis-deno/deploy.png?w=2500&fit=max&auto=format&n=fy-PVAyWJaRFn1UN&q=85&s=547347df1aaece994b978b022e13b038 2500w" />
