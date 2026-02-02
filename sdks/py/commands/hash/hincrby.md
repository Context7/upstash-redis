> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# HINCRBY

> Increments the value of a hash field by a given amount

If the hash field does not exist, it is set to 0 before performing the operation.

## Arguments

<ParamField body="key" type="str" required>
  The key of the hash.
</ParamField>

<ParamField body="field" type="str" required>
  The field to increment
</ParamField>

<ParamField body="increment" type="int">
  How much to increment the field by. Can be negative to subtract.
</ParamField>

## Response

<ResponseField type="int" required>
  The new value of the field after the increment.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.hset("myhash", "field1", 5)

  assert redis.hincrby("myhash", "field1", 10) == 15
  ```
</RequestExample>
