> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Get Started

`@upstash/redis` is written in Deno and can be imported from
[deno.land](https://deno.land)

```ts  theme={"system"}
import { Redis } from "https://deno.land/x/upstash_redis/mod.ts";
```

We transpile the package into an npm compatible package as well:

```bash  theme={"system"}
npm install @upstash/redis
```

```bash  theme={"system"}
yarn add @upstash/redis
```

```bash  theme={"system"}
pnpm add @upstash/redis
```

## Basic Usage:

```ts  theme={"system"}
import { Redis } from "@upstash/redis"

const redis = new Redis({
  url: <UPSTASH_REDIS_REST_URL>,
  token: <UPSTASH_REDIS_REST_TOKEN>,
})

// string
await redis.set('key', 'value');
let data = await redis.get('key');
console.log(data)

await redis.set('key2', 'value2', {ex: 1});

// sorted set
await redis.zadd('scores', { score: 1, member: 'team1' })
data = await redis.zrange('scores', 0, 100 )
console.log(data)

// list
await redis.lpush('elements', 'magnesium')
data = await redis.lrange('elements', 0, 100 )
console.log(data)

// hash
await redis.hset('people', {name: 'joe'})
data = await redis.hget('people', 'name' )
console.log(data)

// sets
await redis.sadd('animals', 'cat')
data  = await redis.spop('animals', 1)
console.log(data)
```
