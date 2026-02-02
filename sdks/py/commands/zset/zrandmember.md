> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# ZRANDMEMBER

> Returns one or more random members from a sorted set, optionally with their scores.

## Arguments

<ParamField body="key" type="str" required>
  The key of the sorted set
</ParamField>

<ParamField body="count" type="int">
  The number of members to return
</ParamField>

<ParamField body="withscores" type="bool">
  Whether to return the scores along with the members
</ParamField>

## Response

<ResponseField type="str | Tuple[str, float] | List[str] | List[Tuple[str, float]]">
  The random member(s) from the sorted set

  If no count is specified, a single member is returned. If count is specified, a list of members is returned.

  If withscores, members are returned as a tuple of (member, score).
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.zadd("myset", {"one": 1, "two": 2, "three": 3})

  # "one"
  redis.zrandmember("myset")

  # ["one", "three"]
  redis.zrandmember("myset", 2)
  ```
</RequestExample>
