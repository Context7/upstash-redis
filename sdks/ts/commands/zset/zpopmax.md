> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# ZPOPMAX

> Removes and returns up to count members with the highest scores in the sorted set stored at key.

## Arguments

<ParamField body="key" type="string" required>
  The key of the sorted set
</ParamField>

## Response

<ResponseField body="count" type="integer">
  The number of elements removed. Defaults to 1.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  const popped = await redis.zpopmax("key", 4);
  ```
</RequestExample>
