> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# DECR

> Decrement the integer value of a key by one

If a key does not exist, it is initialized as 0 before performing the operation. An error is returned if the key contains a value of the wrong type or contains a string that can not be represented as integer.

## Arguments

<ParamField body="key" type="str" required>
  The key to decrement.
</ParamField>

## Response

<ResponseField type="int" required>
  The value at the key after the decrementing.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.set("key", 6)

  assert redis.decr("key") == 5
  ```
</RequestExample>
