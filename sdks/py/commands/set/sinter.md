> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# SINTER

> Return the intersection between sets

## Arguments

<ParamField body="keys" type="*List[str]" required>
  The keys of the sets to perform the intersection operation on.
</ParamField>

## Response

<ResponseField type="set[str]" required>
  The resulting set.
</ResponseField>

<RequestExample>
  ```py Example  theme={"system"}
  redis.sadd("set1", "a", "b", "c"); 
  redis.sadd("set2", "c", "d", "e"); 

  assert redis.sinter("set1", "set2") == {"c"}
  ```
</RequestExample>
