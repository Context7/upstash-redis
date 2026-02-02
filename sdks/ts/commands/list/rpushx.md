> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# RPUSHX

> Push an element at the end of the list only if the list exists.

## Arguments

<ParamField body="key" type="string" required>
  The key of the list.
</ParamField>

<ParamField body="elements" type="...TValue[]" required>
  One or more elements to push at the end of the list.
</ParamField>

## Response

<ResponseField type="number" required>
  The length of the list after the push operation.

  `0` if the list did not exist and thus no element was pushed.
</ResponseField>

<RequestExample>
  ```ts Example  theme={"system"}
  await redis.lpush("key", "a", "b", "c"); 
  const length = await redis.rpushx("key", "d"); 
  console.log(length); // 4
  ```

  ```ts Without existing list  theme={"system"}
  const length = await redis.rpushx("key", "a"); 
  console.log(length); // 0
  ```
</RequestExample>
