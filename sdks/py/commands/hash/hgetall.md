> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# HGETALL

> Retrieves all fields from a hash.

## Arguments

<ParamField body="key" type="str" required>
  The key to get.
</ParamField>

## Response

<ResponseField type="Optional[str]" required>
  An object with all fields in the hash.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.hset("myhash", values={
  "field1": "Hello",
  "field2": "World"
  })

  assert redis.hgetall("myhash") == {"field1": "Hello", "field2": "World"}
  ```
</RequestExample>
