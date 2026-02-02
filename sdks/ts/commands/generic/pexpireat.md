> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# PEXPIREAT

> Sets a timeout on key. After the timeout has expired, the key will automatically be deleted.

## Arguments

<ParamField body="key" type="string" required>
  The key to expire.
</ParamField>

<ParamField body="unixmilli" type="integer">
  The unix timestamp in milliseconds at which the key will expire.
</ParamField>

## Response

<ResponseField type="integer" required>
  `1` if the timeout was applied, `0` if `key` does not exist.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  const 10MinutesFromNow = Date.now() + 10 * 60 * 1000;
   await redis.pexpireat(key, 10MinutesFromNow);
  ```
</RequestExample>
