> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# HMSET

> Write multiple fields to a hash.

## Arguments

<ParamField body="key" type="str" required>
  The key of the hash.
</ParamField>

<ParamField body="fields" type="Dict[str, Any]" required>
  A dictionary of fields and their values.
</ParamField>

## Response

<ResponseField type="int" required>
  The number of fields that were added.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  # Set multiple fields
  assert redis.hset("myhash"{
    "field1": "Hello",
    "field2": "World"
  }) == 2
  ```
</RequestExample>
