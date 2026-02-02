> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# TOUCH

> Alters the last access time of one or more keys

## Arguments

<ParamField body="keys" type="...string[]" required>
  One or more keys.
</ParamField>

## Response

<ResponseField type="integer" required>
  The number of keys that were touched.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  await redis.touch("key1", "key2", "key3");
  ```
</RequestExample>
