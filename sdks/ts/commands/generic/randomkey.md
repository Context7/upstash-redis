> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# RANDOMKEY

> Returns a random key from database

## Arguments

No arguments

## Response

<ResponseField type="string" required>
  A random key from database, or `null` when database is empty.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  const key = await redis.randomkey();
  ```
</RequestExample>
