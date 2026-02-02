> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# HMGET

> Return the requested fields and their values.

## Arguments

<ParamField body="key" type="str" required>
  The key of the hash.
</ParamField>

<ParamField body="fields" type="*List[str]" required>
  One or more fields to get.
</ParamField>

## Response

<ResponseField type="List[str | None]" required>
  An object containing the fields and their values.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.hset("myhash", values={
      "field1": "Hello",
      "field2": "World"
  })

  assert redis.hmget("myhash", "field1", "field2") == ["Hello", "World"]
  ```
</RequestExample>
