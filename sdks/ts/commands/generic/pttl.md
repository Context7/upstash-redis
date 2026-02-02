> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# PTTL

> Return the expiration in milliseconds of a key.

## Arguments

<ParamField body="key" type="string" required>
  The key
</ParamField>

## Response

<ResponseField type="integer" required>
  The number of milliseconds until this expires, negative if the key does not exist or does not have an expiration set.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  const millis = await redis.pttl(key);
  ```
</RequestExample>
