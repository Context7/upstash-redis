> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# HGET

> Retrieves the value of a hash field.

## Arguments

<ParamField body="key" type="string" required>
  The key to get.
</ParamField>

<ParamField body="field" type="string" required>
  The field to get.
</ParamField>

## Response

<ResponseField type="TValue | null" required>
  The value of the field, or `null`, when field is not present in the hash or key does not exist.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  await redis.hset("key", {field: "value"});
  const field = await redis.hget("key", "field");
  console.log(field); // "value"
  ```
</RequestExample>
