> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# GETBIT

> Retrieve a single bit.

## Arguments

<ParamField body="key" type="str" required>
  The key of the bitset
</ParamField>

<ParamField body="offset" type="int" required>
  Specify the offset at which to get the bit.
</ParamField>

## Response

<ResponseField type="int" required>
  The bit value stored at offset.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  bit = redis.getbit(key, 4)
  ```
</RequestExample>
