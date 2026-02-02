> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# SDIFF

> Return the difference between sets

## Arguments

<ParamField body="keys" type="...string[]" required>
  The keys of the sets to perform the difference operation on.
</ParamField>

## Response

<ResponseField type="TValue[]" required>
  The members of the resulting set.
</ResponseField>

<RequestExample>
  ```ts Example  theme={"system"}
  await redis.sadd("set1", "a", "b", "c"); 
  await redis.sadd("set2", "c", "d", "e"); 
  const diff =  await redis.sdiff("set1", "set2");
  console.log(diff); // ["a", "b"]
  ```
</RequestExample>
