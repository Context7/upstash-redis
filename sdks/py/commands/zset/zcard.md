> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# ZCARD

> Returns the number of elements in the sorted set stored at key.

## Arguments

<ParamField body="key" type="str" required>
  The key to get.
</ParamField>

## Response

<ResponseField type="int" required>
  The number of elements in the sorted set.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.zadd("myset", {"one": 1, "two": 2, "three": 3})

  assert redis.zcard("myset") == 3
  ```
</RequestExample>
