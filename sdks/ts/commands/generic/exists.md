> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# EXISTS

> Check if a key exists.

## Arguments

<ParamField body="keys" type="...string[]" required>
  One or more keys to check.
</ParamField>

## Response

<ResponseField type="integer" required>
  The number of keys that exist
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  await redis.set("key1", "value1")
  await redis.set("key2", "value2")
  const keys = await redis.exists("key1", "key2", "key3");
  console.log(keys) // 2
  ```
</RequestExample>
