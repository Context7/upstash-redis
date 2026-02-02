> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# LLEN

> Returns the length of the list stored at key.

## Arguments

<ParamField body="key" type="str" required>
  The key of the list.
</ParamField>

## Response

<ResponseField type="int" required>
  The length of the list at key.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.rpush("key", "a", "b", "c")

  assert redis.llen("key") == 3
  ```
</RequestExample>
