> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# PERSIST

> Remove any timeout set on the key.

## Arguments

<ParamField body="key" type="str" required>
  The key to persist
</ParamField>

## Response

<ResponseField type="bool">
  `True` if the timeout was set
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.set("key1", "Hello")
  redis.expire("key1", 10)

  assert redis.ttl("key1") == 10

  redis.persist("key1")

  assert redis.ttl("key1") == -1
  ```
</RequestExample>
