> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# RANDOMKEY

> Returns a random key from database

## Arguments

No arguments

## Response

<ResponseField type="str">
  A random key from database, or `None` when database is empty.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  assert redis.randomkey() is None

  redis.set("key1", "Hello")
  redis.set("key2", "World")

  assert redis.randomkey() is not None
  ```
</RequestExample>
