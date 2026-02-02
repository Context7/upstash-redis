> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# SDIFFSTORE

> Write the difference between sets to a new set

## Arguments

<ParamField body="destination" type="str" required>
  The key of the set to store the resulting set in.
</ParamField>

<ParamField body="keys" type="*List[str]" required>
  The keys of the sets to perform the difference operation on.
</ParamField>

## Response

<ResponseField type="int" required>
  The number of elements in the resulting set.
</ResponseField>

<RequestExample>
  ```py Example  theme={"system"}
  redis.sadd("key1", "a", "b", "c")

  redis.sadd("key2", "c", "d", "e")

  # Store the result in a new set
  assert redis.sdiffstore("res", "key1", "key2") == 2

  assert redis.smembers("set") == {"a", "b"}
  ```
</RequestExample>
