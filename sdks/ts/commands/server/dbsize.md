> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# DBSIZE

> Count the number of keys in the database.

## Arguments

This command has no arguments

## Response

<ResponseField type="integer" required>
  The number of keys in the database
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  const keys = await redis.dbsize();
  console.log(keys) // 20
  ```
</RequestExample>
