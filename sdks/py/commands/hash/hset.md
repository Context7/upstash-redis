> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# HSET

> Write one or more fields to a hash.

## Arguments

<ParamField body="key" type="str" required>
  The key of the hash.
</ParamField>

<ParamField body="field" type="str">
  Field to set
</ParamField>

<ParamField body="value" type="str">
  Value to set
</ParamField>

<ParamField body="values" type="Dict[str, Any]">
  An object of fields and their values.
</ParamField>

## Response

<ResponseField type="int" required>
  The number of fields that were added.
</ResponseField>

<RequestExample>
  ```py Single theme={"system"}
  # Set a single field
  assert redis.hset("myhash", "field1", "Hello") == 1
  ```

  ```py Multiple theme={"system"}
  # Set multiple fields
  assert redis.hset("myhash", values={
    "field1": "Hello",
    "field2": "World"
  }) == 2
  ```
</RequestExample>
