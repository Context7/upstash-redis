> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# SRANDMEMBER

> Returns one or more random members from a set.

## Arguments

<ParamField body="key" type="str" required>
  The key of the set.
</ParamField>

<ParamField body="count" type="number" default={1}>
  How many members to return.
</ParamField>

## Response

<ResponseField type="TMember | TMember[]" required>
  The random member.
  If `count` is specified, an array of members is returned.
</ResponseField>

<RequestExample>
  ```py Single theme={"system"}
  redis.sadd("myset", "one", "two", "three")

  assert redis.srandmember("myset") in {"one", "two", "three"}
  ```

  ```py With Count  theme={"system"}
  redis.sadd("myset", "one", "two", "three")

  assert redis.srandmember("myset", 2) in {"one", "two", "three"}
  ```
</RequestExample>
