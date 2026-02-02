> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# HEXISTS

> Checks if a field exists in a hash.

## Arguments

<ParamField body="key" type="str" required>
  The key to get.
</ParamField>

<ParamField body="field" type="str" required>
  The field to check.
</ParamField>

## Response

<ResponseField type="bool" required>
  `True` if the hash contains `field`. `False` if the hash does not contain `field`, or `key` does not exist.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.hset("key", "field", "value")

  assert redis.hexists("key", "field") == True
  ```
</RequestExample>
