> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# ZDIFFSTORE

> Writes the difference between sets to a new key.

## Arguments

<ParamField body="destination" type="str" required>
  The key to write the difference to.
</ParamField>

<ParamField body="keys" type="List[str]" required>
  The keys to compare.
</ParamField>

## Response

<ResponseField type="int">
  The number of elements in the resulting set.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.zadd("key1", {"a": 1, "b": 2, "c": 3})

  redis.zadd("key2", {"c": 3, "d": 4, "e": 5})

  # a and b
  assert redis.zdiffstore("dest", ["key1", "key2"]) == 2
  ```
</RequestExample>
