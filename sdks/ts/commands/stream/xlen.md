> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# XLEN

> Returns the number of entries inside a stream.

## Arguments

<ParamField body="key" type="string" required>
  The key of the stream.
</ParamField>

## Response

<ResponseField type="number">
  The number of entries in the stream. Returns 0 if the stream does not exist.
</ResponseField>

<RequestExample>
  ```ts Get stream length theme={"system"}
  const result = await redis.xlen("mystream");
  ```
</RequestExample>
