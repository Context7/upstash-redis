> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# ZREM

> Remove one or more members from a sorted set

## Arguments

<ParamField body="key" type="str" required>
  The key of the sorted set
</ParamField>

<ParamField body="members" type="*List[str]" required>
  One or more members to remove
</ParamField>

## Response

<ResponseField required>
  The number of members removed from the sorted set.
</ResponseField>

<RequestExample>
  ```py Single theme={"system"}
  redis.zadd("myset", {"one": 1, "two": 2, "three": 3})

  assert redis.zrem("myset", "one", "four") == 1
  ```
</RequestExample>
