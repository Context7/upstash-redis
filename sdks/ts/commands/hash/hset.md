> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# HSET

> Write one or more fields to a hash.

## Arguments

<ParamField body="key" type="string" required>
  The key of the hash.
</ParamField>

<ParamField body="fields" type="{ [fieldName]: TValue }" required>
  An object of fields and their values.
</ParamField>

## Response

<ResponseField type="integer" required>
  The number of fields that were added.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  await redis.hset("key", {
    id: 1,
    username: "chronark",
    name: "andreas"
    });
  ```
</RequestExample>
