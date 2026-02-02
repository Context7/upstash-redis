> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Connect Your Client

Upstash works with Redis® API, that means you can use any Redis client with
Upstash. At the [Redis Clients](https://redis.io/clients) page you can find the
list of Redis clients in different languages.

Probably, the easiest way to connect to your database is to use `redis-cli`.
Because it is already covered in [Getting Started](../overall/getstarted), we
will skip it here.

## Database

After completing the [getting started](../overall/getstarted) guide, you will
see the database page as below:

<Frame>
  <img src="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/database.png?fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=4530264625c10bdf334129ec8b367511" data-og-width="1590" width="1590" data-og-height="1080" height="1080" data-path="img/getting_started/database.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/database.png?w=280&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=729b8c0843969c86866b06e22747c785 280w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/database.png?w=560&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=d44be677d29134227ff6839fbfc10674 560w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/database.png?w=840&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=414a590eb3c8ed98001a5a781a6268bf 840w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/database.png?w=1100&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=eca30f6532a78f7f25952b41beac50d5 1100w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/database.png?w=1650&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=e60ccc845ab5a2a2b4fb9d66ac0fe948 1650w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/database.png?w=2500&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=b999e96686847b5aeeebc960cf2d5a30 2500w" />
</Frame>

The information required for Redis clients is displayed here as **Endpoint**,
**Port** and **Password**. Also when you click on `Clipboard` button on **Connect to your database** section, you can copy
the code that is required for your client.

Below, we will provide examples from popular Redis clients, but the information above should help you configure all Redis clients similarly.

<Note>
  TLS is enabled by default for all Upstash Redis databases. It's not possible
  to disable it.
</Note>

## upstash-redis

<Info>
  Because upstash-redis is HTTP based, we recommend it for Serverless functions.
  Other TCP based clients can cause connection problems in highly concurrent use
  cases.
</Info>

**Library**: [upstash-redis](https://github.com/upstash/upstash-redis)

**Example**:

```typescript  theme={"system"}
import { Redis } from "@upstash/redis";

const redis = new Redis({
  url: "UPSTASH_REDIS_REST_URL",
  token: "UPSTASH_REDIS_REST_TOKEN",
});

(async () => {
  try {
    const data = await redis.get("key");
    console.log(data);
  } catch (error) {
    console.error(error);
  }
})();
```

## Node.js

**Library**: [ioredis](https://github.com/luin/ioredis)

**Example**:

```javascript  theme={"system"}
const Redis = require("ioredis");

let client = new Redis("rediss://:YOUR_PASSWORD@YOUR_ENDPOINT:YOUR_PORT");
await client.set("foo", "bar");
let x = await client.get("foo");
console.log(x);
```

## Python

**Library**: [redis-py](https://github.com/andymccurdy/redis-py)

**Example**:

```python  theme={"system"}
import redis
r = redis.Redis(
host= 'YOUR_ENDPOINT',
port= 'YOUR_PORT',
password= 'YOUR_PASSWORD',
ssl=True)
r.set('foo','bar')
print(r.get('foo'))
```

## Java

**Library**: [jedis](https://github.com/xetorthio/jedis)

**Example**:

```java  theme={"system"}
Jedis jedis = new Jedis("YOUR_ENDPOINT", "YOUR_PORT", true);
jedis.auth("YOUR_PASSWORD");
jedis.set("foo", "bar");
String value = jedis.get("foo");
System.out.println(value);
```

<Info>
  Jedis does not offer command level retry config by default, but you can handle
  retries using connection pool. Check [Retrying a command after a connection
  failure](https://redis.io/docs/latest/develop/clients/jedis/connect/#retrying-a-command-after-a-connection-failure)
</Info>

## PHP

**Library**: [phpredis](https://github.com/phpredis/phpredis)

**Example**:

```php  theme={"system"}
<?php

$redis = new Redis();

$redis->connect("YOUR_ENDPOINT", "YOUR_PORT");
$redis->auth("YOUR_PASSWORD");

$redis->set("foo", "bar");

print_r($redis->get("foo"));
```

<Info>
  Phpredis supports connection level retries through `OPT_MAX_RETRIES`. However,
  for command level retries, it only supports [SCAN
  command](https://github.com/phpredis/phpredis?tab=readme-ov-file#example-29).
</Info>

## Go

**Library**: [redigo](https://github.com/gomodule/redigo)

**Example**:

```go  theme={"system"}
func main() {
  c, err := redis.Dial("tcp", "YOUR_ENDPOINT:YOUR_PORT", redis.DialUseTLS(true))
  if err != nil {
      panic(err)
  }

  _, err = c.Do("AUTH", "YOUR_PASSWORD")
  if err != nil {
      panic(err)
  }

  _, err = c.Do("SET", "foo", "bar")
  if err != nil {
      panic(err)
  }

  value, err := redis.String(c.Do("GET", "foo"))
  if err != nil {
      panic(err)
  }

  println(value)
}
```
