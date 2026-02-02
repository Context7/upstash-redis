> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# EXISTS

> Check if a key exists.

## Arguments

<ParamField body="keys" type="*List[str]" required>
  One or more keys to check.
</ParamField>

## Response

<ResponseField type="int" required>
  The number of keys that exist
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.set("key1", "Hello")
  redis.set("key2", "World")

  assert redis.exists("key1", "key2") == 2

  redis.delete("key1")

  assert redis.exists("key1", "key2") == 1
  ```
</RequestExample>
