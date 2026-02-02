> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# PEXPIRE

> Sets a timeout on key. After the timeout has expired, the key will automatically be deleted.

## Arguments

<ParamField body="key" type="string" required>
  The key to expire.
</ParamField>

<ParamField body="milliseconds" type="integer">
  The number of milliseconds until the key expires.
</ParamField>

## Response

<ResponseField type="integer" required>
  `1` if the timeout was applied, `0` if `key` does not exist.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
   await redis.pexpire(key, 60_000); // 1 minute
  ```
</RequestExample>
