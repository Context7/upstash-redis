> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# HRANDFIELD

> Return a random field from a hash

## Arguments

<ParamField body="key" type="string" required>
  The key of the hash.
</ParamField>

<ParamField body="count" type="integer">
  Optionally return more than one field.
</ParamField>

<ParamField body="withValues" type="boolean">
  Return the values of the fields as well.
</ParamField>

## Response

<ResponseField type="Record<string, unknown>" required>
  An object containing the fields and their values.
</ResponseField>

<RequestExample>
  ```ts Basic theme={"system"}
  await redis.hset("key", {
    id: 1,
    username: "chronark",
    name: "andreas"
   });
  const randomField = await redis.hrandfield("key");
  console.log(randomField); // one of "id", "username" or  "name"
  ```

  ```ts Multiple Fields theme={"system"}
  await redis.hset("key", {
    id: 1,
    username: "chronark",
    name: "andreas",
  });
  const randomFields = await redis.hrandfield("key", 2);
  console.log(randomFields); // ["id", "username"] or any other combination
  ```

  ```ts With Values theme={"system"}
  await redis.hset("key", {
    id: 1,
    username: "chronark",
    name: "andreas",
  });
  const randomFields = await redis.hrandfield("key", 2, true);
  console.log(randomFields); // { id: "1", username: "chronark" } or any other combination
  ```
</RequestExample>
