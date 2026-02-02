> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# SINTER

> Return the intersection between sets and store the resulting set in a key

## Arguments

<ParamField body="destination" type="str" required>
  The key of the set to store the resulting set in.
</ParamField>

<ParamField body="keys" type="*List[str]" required>
  The keys of the sets to perform the intersection operation on.
</ParamField>

## Response

<ResponseField type="int" required>
  The number of elements in the resulting set.
</ResponseField>

<RequestExample>
  ```py Example  theme={"system"}
  redis.sadd("set1", "a", "b", "c"); 

  redis.sadd("set2", "c", "d", "e"); 

  assert redis.sinter("destination", "set1", "set2") == 1
  ```
</RequestExample>
