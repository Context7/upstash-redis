> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# HINCRBY

> Increments the value of a hash field by a given amount

## Arguments

<ParamField body="key" type="string" required>
  The key of the hash.
</ParamField>

<ParamField body="field" type="string" required>
  The field to increment
</ParamField>

<ParamField body="increment" type="integer" required>
  How much to increment the field by. Can be negative to subtract.
</ParamField>

## Response

<ResponseField type="integer" required>
  The new value of the field after the increment.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  await redis.hset("key", {
    field: 20,
    });
  const after = await redis.hincrby("key", "field", 2);
  console.log(after); // 22
  ```
</RequestExample>
