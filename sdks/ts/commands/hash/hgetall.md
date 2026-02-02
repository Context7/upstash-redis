> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# HGETALL

> Retrieves all fields from a hash.

## Arguments

<ParamField body="key" type="string" required>
  The key to get.
</ParamField>

## Response

<ResponseField type="TValue | null" required>
  An object with all fields in the hash.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  await redis.hset("key", {
    field1: "value1",
    field2: "value2",
    });
  const hash = await redis.hgetall("key");
  console.log(hash); // { field1: "value1", field2: "value2" }
  ```
</RequestExample>
