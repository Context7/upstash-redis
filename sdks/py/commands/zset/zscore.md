> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# ZSCORE

> Returns the scores of a member.

## Arguments

<ParamField body="key" type="str" required>
  The key to get.
</ParamField>

## Response

<ResponseField body="member" type="TMember" required>
  A member of the sortedset.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.zadd("myset", {"a": 1, "b": 2, "c": 3})

  assert redis.zscore("myset", "a") == 1
  ```
</RequestExample>
