> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# MGET

> Load multiple keys from Redis in one go.

For billing purposes, this counts as a single command.

## Arguments

<ParamField body="keys" type="*List[str]" required>
  Multiple keys to load from Redis.
</ParamField>

## Response

<ResponseField type="List[str]" required>
  An array of values corresponding to the keys passed in. If a key doesn't exist, the value will be `None`.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.set("key1", "value1")

  redis.set("key2", "value2")

  assert redis.mget("key1", "key2") == ["value1", "value2"]
  ```
</RequestExample>
