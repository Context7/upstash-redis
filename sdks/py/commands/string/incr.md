> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# INCR

> Increment the integer value of a key by one

If a key does not exist, it is initialized as 0 before performing the operation. An error is returned if the key contains a value of the wrong type or contains a string that can not be represented as integer.

## Arguments

<ParamField body="key" type="str" required>
  The key to increment.
</ParamField>

## Response

<ResponseField type="int" required>
  The value at the key after the incrementing.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.set("key", 6)

  assert redis.incr("key") == 7
  ```
</RequestExample>
