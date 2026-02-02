> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# DrizzleORM with Upstash Redis

### Quickstart

DrizzleORM provides an `upstashCache()` helper to easily connect with Upstash Redis. To prevent surprises, the cache is always opt-in by default. Nothing is cached until you opt-in for a specific query or enable global caching.

First, install the drizzle package:

```bash  theme={"system"}
npm install drizzle-orm
```

**Configure your Drizzle instance:**

```ts  theme={"system"}
import { upstashCache } from "drizzle-orm/cache/upstash"
import { drizzle } from "drizzle-orm/..."

const db = drizzle(process.env.DB_URL!, {
  cache: upstashCache(),
})
```

You can also explicitly define your Upstash credentials, enable global caching for all queries by default (opt-out) or pass custom caching options:

```ts  theme={"system"}
import { upstashCache } from "drizzle-orm/cache/upstash"
import { drizzle } from "drizzle-orm/..."

const db = drizzle(process.env.DB_URL!, {
  cache: upstashCache({
    // 👇 Redis credentials (optional — can also be pulled from env vars)
    url: "<UPSTASH_URL>",
    token: "<UPSTASH_TOKEN>",
    // 👇 Enable caching for all queries (optional, default false)
    global: true,
    // 👇 Default cache behavior (optional)
    config: { ex: 60 },
  }),
})
```

***

### Cache Behavior

* **Per-query caching (opt-in, default):**\
  No queries are cached unless you explicitly call `.$withCache()`.

  ```ts  theme={"system"}
  await db.insert(users).value({ email: "cacheman@upstash.com" });

  // 👇 reads from cache
  await db.select().from(users).$withCache()
  ```

* **Global caching:**\
  When setting `global: true`, all queries will read from cache by default.

  ```ts  theme={"system"}
  const db = drizzle(process.env.DB_URL!, {
    cache: upstashCache({ global: true }),
  })

  // 👇 reads from cache (no more explicit `$withCache()`)
  await db.select().from(users)
  ```

  You can always turn off caching for a specific query:

  ```ts  theme={"system"}
  await db.select().from(users).$withCache(false)
  ```

***

### Manual Cache Invalidation

Cache invalidation is fully automatic by default. If you ever need to, you can manually invalidate cached queries by table name or custom tags:

```ts  theme={"system"}
// 👇 invalidate all queries that use the `users` table
await db.$cache?.invalidate({ tables: ["usersTable"] })

// 👇 invalidate all queries by custom tag (defined in previous queries)
await db.$cache?.invalidate({ tags: ["custom_key"] })
```

***

For more details on this integration, refer to the [Drizzle ORM caching documentation](https://cache.drizzle-orm-fe.pages.dev/docs/cache).
