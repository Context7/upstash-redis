> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# PTTL

> Return the expiration in milliseconds of a key.

## Arguments

<ParamField body="key" type="str" required>
  The key
</ParamField>

## Response

<ResponseField type="int" required>
  The number of milliseconds until this expires, negative if the key does not exist or does not have an expiration set.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.set("key1", "Hello")

  assert redis.pttl("key1") == -1

  redis.expire("key1", 1000)

  assert redis.pttl("key1") > 0

  redis.persist("key1")

  assert redis.pttl("key1") == -1
  ```
</RequestExample>
