> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# SETBIT

> Set a single bit in a string.

## Arguments

<ParamField body="key" type="str" required>
  The key of the bitset
</ParamField>

<ParamField body="offset" type="int" required>
  Specify the offset at which to set the bit.
</ParamField>

<ParamField body="value" type="0 | 1" required>
  The bit to set
</ParamField>

## Response

<ResponseField type="0 | 1" required>
  The original bit value stored at offset.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  original_bit = redis.setbit(key, 4, 1)
  ```
</RequestExample>
