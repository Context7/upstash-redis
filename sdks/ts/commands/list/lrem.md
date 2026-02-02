> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# LREM

> Remove the first `count` occurrences of an element from a list.

## Arguments

<ParamField body="key" type="string" required>
  The key of the list.
</ParamField>

<ParamField body="count" type="number" required>
  How many occurrences of the element to remove.
</ParamField>

<ParamField body="element" type="TValue" required>
  The element to remove
</ParamField>

## Response

<ResponseField type="integer" required>
  The number of elements removed.
</ResponseField>

<RequestExample>
  ```ts Example  theme={"system"}
  await redis.lpush("key", "a", "a", "b", "b", "c"); 
  const removed = await redis.lrem("key", 4, "b"); 
  console.log(removed) // 2
  ```
</RequestExample>
