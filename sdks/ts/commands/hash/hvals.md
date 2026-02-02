> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# HVALS

> Returns all values in the hash stored at key.

## Arguments

<ParamField body="key" type="string" required>
  The key of the hash.
</ParamField>

## Response

<ResponseField type="unknown[]" required>
  All values in the hash, or an empty list when key does not exist.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  await redis.hset("key", {
    field1: "Hello",
    field2: "World",
  })
  const values = await redis.hvals("key")
  console.log(values) // ["Hello", "World"]
  ```
</RequestExample>
