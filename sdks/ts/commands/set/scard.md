> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# SCARD

> Return how many members are in a set

## Arguments

<ParamField body="key" type="string" required>
  The key of the set.
</ParamField>

## Response

<ResponseField type="number" required>
  How many members are in the set.
</ResponseField>

<RequestExample>
  ```ts Example  theme={"system"}
  await redis.sadd("key", "a", "b", "c"); 
  const cardinality = await redis.scard("key");
  console.log(cardinality); // 3
  ```
</RequestExample>
