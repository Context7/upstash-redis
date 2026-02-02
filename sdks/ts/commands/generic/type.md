> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# TYPE

> Get the type of a key.

## Arguments

<ParamField body="key" type="string" required>
  The key to get.
</ParamField>

## Response

<ResponseField type="string" required>
  The type of the key.

  One of `string` | `list` | `set` | `zset` | `hash` | `none`
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  await redis.set("key", "value");
  const t = await redis.type("key");
  console.log(t) // "string"
  ```
</RequestExample>
