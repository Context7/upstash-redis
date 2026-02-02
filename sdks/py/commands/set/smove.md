> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# SMOVE

> Move a member from one set to another

## Arguments

<ParamField body="source" type="str" required>
  The key of the set to move the member from.
</ParamField>

<ParamField body="destination" type="str" required>
  The key of the set to move the member to.
</ParamField>

<ParamField body="member" type="str">
  The members to move
</ParamField>

## Response

<ResponseField type="bool" required>
  `True` if the member was moved, `False` if it was not.
</ResponseField>

<RequestExample>
  ```py Example  theme={"system"}
  redis.sadd("src", "one", "two", "three")

  redis.sadd("dest", "four")

  assert redis.smove("src", "dest", "three") == True

  assert redis.smembers("source") == {"one", "two"}

  assert redis.smembers("destination") == {"three", "four"}
  ```
</RequestExample>
