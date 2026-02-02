> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# SMISMEMBER

> Check if multiple members exist in a set

## Arguments

<ParamField body="key" type="str" required>
  The key of the set to check.
</ParamField>

<ParamField body="members" type="TMember[]">
  The members to check
</ParamField>

## Response

<ResponseField type="List[bool]" required>
  An array of `True` and `False` values.
  `True` if the member exists in the set, `False` if not.
</ResponseField>

<RequestExample>
  ```py Example  theme={"system"}
  redis.sadd("myset", "one", "two", "three")

  assert redis.smismember("myset", "one", "four") == [True, False]

  assert redis.smismember("myset", "four", "five") == [False, False]
  ```
</RequestExample>
