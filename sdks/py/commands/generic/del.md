> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# DEL

> Removes the specified keys. A key is ignored if it does not exist.

## Arguments

<ParamField body="keys" type="*List[str]" required>
  One or more keys to remove.
</ParamField>

## Response

<ResponseField type="int" required>
  The number of keys that were removed.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.set("key1", "Hello")
  redis.set("key2", "World")
  redis.delete("key1", "key2")

  assert redis.get("key1") is None
  assert redis.get("key2") is None
  ```
</RequestExample>
