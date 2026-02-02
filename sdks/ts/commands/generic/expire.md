> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# EXPIRE

> Sets a timeout on key. The key will automatically be deleted.

## Arguments

<ParamField body="key" type="string" required>
  The key to set the timeout on.
</ParamField>

<ParamField body="seconds" type="integer">
  How many seconds until the key should be deleted.
</ParamField>

## Response

<ResponseField type="integer" required>
  `1` if the timeout was set, `0` otherwise
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  await redis.set("mykey", "Hello");
  await redis.expire("mykey", 10);
  ```
</RequestExample>
