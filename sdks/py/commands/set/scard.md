> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# SCARD

> Return how many members are in a set

## Arguments

<ParamField body="key" type="str" required>
  The key of the set.
</ParamField>

## Response

<ResponseField type="int" required>
  How many members are in the set.
</ResponseField>

<RequestExample>
  ```py Example  theme={"system"}
  redis.sadd("key", "a", "b", "c"); 

  assert redis.scard("key") == 3
  ```
</RequestExample>
