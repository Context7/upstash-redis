> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# ZINCRBY

> Increment the score of a member.

## Arguments

<ParamField body="key" type="str" required>
  The key of the sorted set.
</ParamField>

<ParamField body="increment" type="int" required>
  The increment to add to the score.
</ParamField>

<ParamField body="member" type="str" required>
  The member to increment.
</ParamField>

## Response

<ResponseField type="float" required>
  The new score of `member` after the increment operation.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.zadd("myset", {"one": 1, "two": 2, "three": 3})

  assert redis.zincrby("myset", 2, "one") == 3
  ```
</RequestExample>
