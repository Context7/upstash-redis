> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# HKEYS

> Return all field names in the hash stored at key.

## Arguments

<ParamField body="key" type="str" required>
  The key of the hash.
</ParamField>

## Response

<ResponseField type="List[str]" required>
  The field names of the hash
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.hset("myhash", values={
      "field1": "Hello",
      "field2": "World"
  })

  assert redis.hkeys("myhash") == ["field1", "field2"]
  ```
</RequestExample>
