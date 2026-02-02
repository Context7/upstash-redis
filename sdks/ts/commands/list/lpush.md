> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# LPUSH

> Push an element at the head of the list.

## Arguments

<ParamField body="key" type="string" required>
  The key of the list.
</ParamField>

<ParamField body="elements" type="...TValue[]" required>
  One or more elements to push at the head of the list.
</ParamField>

## Response

<ResponseField type="number" required>
  The length of the list after the push operation.
</ResponseField>

<RequestExample>
  ```ts Example  theme={"system"}
  const length1 = await redis.lpush("key", "a", "b", "c"); 
  console.log(length1); // 3
  const length2 = await redis.lpush("key", "d"); 
  console.log(length2); // 4
  ```
</RequestExample>
