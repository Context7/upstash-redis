> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# App Router

***

## Quickstart: Upstash Redis in Next 15

<Frame>
  <iframe src="https://player.mux.com/gPYmP1M00800UgLr4fa9O8CeN6M36E2iY6Bww8Ir5Qn4U?thumbnail-time=5&metadata-video-title=Upstash+Redis+x+Next+15+Quickstart&video-title=Upstash+Redis+x+Next+15+Quickstart" allow="accelerometer; gyroscope; autoplay; encrypted-media; fullscreen;" allowfullscreen className="w-full aspect-video" />
</Frame>

***

## 1. Install package

In your Next.js app, install our `@upstash/redis` package:

```bash  theme={"system"}
npm install @upstash/redis
```

***

## 2. Connect to Redis

1. Grab your Redis credentials from the Upstash dashboard

   <Frame>
     <img src="https://mintcdn.com/upstash/jtc3r6kD_firFPfY/img/next-quickstart/credentials.png?fit=max&auto=format&n=jtc3r6kD_firFPfY&q=85&s=9579b4b5bdffebf8fc826afb27dbade0" data-og-width="1465" width="1465" data-og-height="392" height="392" data-path="img/next-quickstart/credentials.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/jtc3r6kD_firFPfY/img/next-quickstart/credentials.png?w=280&fit=max&auto=format&n=jtc3r6kD_firFPfY&q=85&s=dd43bbd32b2f717411a9e9224d011ecc 280w, https://mintcdn.com/upstash/jtc3r6kD_firFPfY/img/next-quickstart/credentials.png?w=560&fit=max&auto=format&n=jtc3r6kD_firFPfY&q=85&s=ad29f55a2af986d3d60f951eeca48ce9 560w, https://mintcdn.com/upstash/jtc3r6kD_firFPfY/img/next-quickstart/credentials.png?w=840&fit=max&auto=format&n=jtc3r6kD_firFPfY&q=85&s=fdc958de0ac98113944ea845e21cf6a5 840w, https://mintcdn.com/upstash/jtc3r6kD_firFPfY/img/next-quickstart/credentials.png?w=1100&fit=max&auto=format&n=jtc3r6kD_firFPfY&q=85&s=aaf5a153a3c3e820e392596d044e9ab5 1100w, https://mintcdn.com/upstash/jtc3r6kD_firFPfY/img/next-quickstart/credentials.png?w=1650&fit=max&auto=format&n=jtc3r6kD_firFPfY&q=85&s=e824c0be82bfa51b7726c54bc672821b 1650w, https://mintcdn.com/upstash/jtc3r6kD_firFPfY/img/next-quickstart/credentials.png?w=2500&fit=max&auto=format&n=jtc3r6kD_firFPfY&q=85&s=c1c12586cf4fe6fbce09cfd07d893a2c 2500w" />
   </Frame>

2. Paste them into your Next environment variables:

   ```bash title=".env" theme={"system"}
   UPSTASH_REDIS_REST_URL=https://holy-kite-17499.upstash.io
   UPSTASH_REDIS_REST_TOKEN=AURbAAIncDEyYjM4M...
   ```

3. Create a Redis instance, for example in `lib/redis.ts`

   ```typescript title="lib/redis.ts" theme={"system"}
   import { Redis } from "@upstash/redis"

   // 👇 we can now import our redis client anywhere we need it
   export const redis = new Redis({
     url: process.env.UPSTASH_REDIS_REST_URL,
     token: process.env.UPSTASH_REDIS_REST_TOKEN,
   })
   ```

***

## 3. Using our Redis Client

We can now connect to Upstash Redis from any server component or API route. For example:

```typescript title="app/page.tsx" theme={"system"}
import { redis } from "@/lib/redis"

// 👇 server component
const Page = async () => {
  const count = await redis.get<number>("count")
  return <p>count: {count}</p>
}

export default Page
```

Because this `count` doesn't exist yet, let's create a Next API route to populate it.

***

## 3. Storing data in Redis

Let's create a super simple API that, every time when called, increments an integer value we call `count`. This is the same value we display in our page above:

```typescript title="app/api/counter/route.ts" theme={"system"}
import { redis } from "@/lib/redis"

export const POST = async () => {
  await redis.incr("count")

  return new Response("OK")
}
```

Perfect! Every time we now call this API, we increment the count in our Redis database:

<Frame>
  <img src="https://mintcdn.com/upstash/jtc3r6kD_firFPfY/img/next-quickstart/curl.png?fit=max&auto=format&n=jtc3r6kD_firFPfY&q=85&s=76efae06a8805d53c457726204f61c73" data-og-width="953" width="953" data-og-height="108" height="108" data-path="img/next-quickstart/curl.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/jtc3r6kD_firFPfY/img/next-quickstart/curl.png?w=280&fit=max&auto=format&n=jtc3r6kD_firFPfY&q=85&s=90fab89a9e93352d33f1cb45ead14529 280w, https://mintcdn.com/upstash/jtc3r6kD_firFPfY/img/next-quickstart/curl.png?w=560&fit=max&auto=format&n=jtc3r6kD_firFPfY&q=85&s=3a5fe449bc5ce81186a9de193ad016e3 560w, https://mintcdn.com/upstash/jtc3r6kD_firFPfY/img/next-quickstart/curl.png?w=840&fit=max&auto=format&n=jtc3r6kD_firFPfY&q=85&s=d01de44348f675b6feccb72667cbb0ce 840w, https://mintcdn.com/upstash/jtc3r6kD_firFPfY/img/next-quickstart/curl.png?w=1100&fit=max&auto=format&n=jtc3r6kD_firFPfY&q=85&s=d40e207b189ec138e5fea53818fb9e4c 1100w, https://mintcdn.com/upstash/jtc3r6kD_firFPfY/img/next-quickstart/curl.png?w=1650&fit=max&auto=format&n=jtc3r6kD_firFPfY&q=85&s=6e2b43c93cb4a6fbb0817fc70267072a 1650w, https://mintcdn.com/upstash/jtc3r6kD_firFPfY/img/next-quickstart/curl.png?w=2500&fit=max&auto=format&n=jtc3r6kD_firFPfY&q=85&s=c9b9118267f9de0e28b40e6a2039de47 2500w" />
</Frame>

The server component fetches the most recent count at render-time and displays the up-to-date value automatically. For a video demo, check the video at the top of this article.

***

## Examples

<Card title="GitHub Repository" icon="github" href="https://github.com/upstash/redis-js/tree/main/examples/nextjs-app-router" horizontal>
  You can find the project source code on GitHub.
</Card>

<Info>
  If you're already on Vercel, you can create Upstash projects directly through Vercel: [Read more](../howto/vercelintegration).
</Info>
