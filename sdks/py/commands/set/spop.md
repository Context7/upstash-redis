> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# SPOP

> Removes and returns one or more random members from a set.

## Arguments

<ParamField body="key" type="str" required>
  The key of the set.
</ParamField>

<ParamField body="count" type="int">
  How many members to remove and return.
</ParamField>

## Response

<ResponseField type="str | set[str]" required>
  The popped member.
  If `count` is specified, a set of members is returned.
</ResponseField>

<RequestExample>
  ```py Single theme={"system"}
  redis.sadd("myset", "one", "two", "three")

  assert redis.spop("myset") in {"one", "two", "three"}
  ```

  ```py With Count  theme={"system"}
  redis.sadd("myset", "one", "two", "three")

  assert redis.spop("myset", 2) in {"one", "two", "three"}
  ```
</RequestExample>
