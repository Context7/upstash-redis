> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# BITPOS

> Find the position of the first set or clear bit (bit with a value of 1 or 0) in a Redis string key.

## Arguments

<ParamField body="key" type="str" required>
  The key to search in.
</ParamField>

<ParamField body="bit" type="0 | 1" required>
  The key to store the result of the operation in.
</ParamField>

<ParamField body="start" type="int">
  The index to start searching at.
</ParamField>

<ParamField body="end" type="int">
  The index to stop searching at.
</ParamField>

## Response

<ResponseField type="int" required>
  The index of the first occurrence of the bit in the string.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.setbit("mykey", 7, 1)
  redis.setbit("mykey", 8, 1)

  assert redis.bitpos("mykey", 1) == 7
  assert redis.bitpos("mykey", 0) == 0

  # With a range
  assert redis.bitpos("mykey", 1, 0, 2) == 0
  assert redis.bitpos("mykey", 1, 2, 3) == -1
  ```

  ```py With Range theme={"system"}
  redis.bitpos("key", 1, 5, 20)
  ```
</RequestExample>
