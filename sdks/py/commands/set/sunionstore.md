> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# SUNIONSTORE

> Return the union between sets and store the resulting set in a key

## Arguments

<ParamField body="destination" type="str" required>
  The key of the set to store the resulting set in.
</ParamField>

<ParamField body="keys" type="*List[str]" required>
  The keys of the sets to perform the union operation on.
</ParamField>

## Response

<ResponseField type="set[str]" required>
  The members of the resulting set.
</ResponseField>

<RequestExample>
  ```py Example  theme={"system"}
  redis.sadd("set1", "a", "b", "c"); 
  redis.sadd("set2", "c", "d", "e"); 
  redis.sunionstore("destination", "set1", "set2")
  ```
</RequestExample>
