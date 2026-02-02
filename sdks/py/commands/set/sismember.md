> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# SISMEMBER

> Check if a member exists in a set

## Arguments

<ParamField body="key" type="str" required>
  The key of the set to check.
</ParamField>

<ParamField body="member" type="str">
  The member to check for.
</ParamField>

## Response

<ResponseField type="bool" required>
  `True` if the member exists in the set, `False` if not.
</ResponseField>

<RequestExample>
  ```py Example  theme={"system"}
  redis.sadd("set", "a", "b", "c")

  assert redis.sismember("set", "a") == True
  ```
</RequestExample>
