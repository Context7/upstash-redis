> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# HGET

> Retrieves the value of a hash field.

## Arguments

<ParamField body="key" type="str" required>
  The key to get.
</ParamField>

<ParamField body="field" type="str" required>
  The field to get.
</ParamField>

## Response

<ResponseField type="Optional[str]">
  The value of the field, or `null`, when field is not present in the hash or key does not exist.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.hset("myhash", "field1", "Hello")

  assert redis.hget("myhash", "field1") == "Hello"
  assert redis.hget("myhash", "field2") is None
  ```
</RequestExample>
