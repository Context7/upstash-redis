> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# HMGET

> Return the requested fields and their values.

## Arguments

<ParamField body="key" type="string" required>
  The key of the hash.
</ParamField>

<ParamField body="fields" type="...string[]" required>
  One or more fields to get.
</ParamField>

## Response

<ResponseField type="Record<string, unknown>" required>
  An object containing the fields and their values.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  await redis.hset("key", {
    id: 1,
    username: "chronark",
    name: "andreas"
    });
  const fields = await redis.hmget("key", "username", "name");
  console.log(fields); // { username: "chronark", name: "andreas" }
  ```
</RequestExample>
