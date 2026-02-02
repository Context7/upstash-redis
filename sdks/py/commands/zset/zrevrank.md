> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# ZREVRANK

> Returns the rank of a member in a sorted set, with scores ordered from high to low.

## Arguments

<ParamField body="key" type="str" required>
  The key to get.
</ParamField>

<ParamField body="member" type="str" required>
  The member to get the reverse rank of.
</ParamField>

## Response

<ResponseField type="int" required>
  The reverse rank of the member.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.zadd("myset", {"a": 1, "b": 2, "c": 3})

  assert redis.zrevrank("myset", "a") == 2
  ```
</RequestExample>
