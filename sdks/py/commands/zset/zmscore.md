> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# ZMSCORE

> Returns the scores of multiple members.

## Arguments

<ParamField body="key" type="str" required>
  The key of the sorted set.
</ParamField>

## Response

<ResponseField body="members" type="List[str]" required>
  The members of the sorted set.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.zadd("myset", {"a": 1, "b": 2, "c": 3})

  assert redis.zlexcount("myset", "-", "+") == 3
  ```
</RequestExample>
