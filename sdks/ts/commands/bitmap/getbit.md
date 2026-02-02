> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# GETBIT

> Retrieve a single bit.

## Arguments

<ParamField body="key" type="string" required>
  The key of the bitset
</ParamField>

<ParamField body="offset" type="integer" required>
  Specify the offset at which to get the bit.
</ParamField>

## Response

<ResponseField type="integer" required>
  The bit value stored at offset.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  const bit = await redis.getbit(key, 4);
  ```
</RequestExample>
