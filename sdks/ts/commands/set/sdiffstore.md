> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# SDIFFSTORE

> Write the difference between sets to a new set

## Arguments

<ParamField body="destination" type="string" required>
  The key of the set to store the resulting set in.
</ParamField>

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
  await redis.sdiff("dest", "set1", "set2");
  console.log(diff); // ["a", "b"]
  ```
</RequestExample>
