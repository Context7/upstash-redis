> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# GETRANGE

> Return a substring of value at the specified key.

## Arguments

<ParamField body="key" type="str" required>
  The key to get.
</ParamField>

<ParamField body="start" type="int" required>
  The start index of the substring.
</ParamField>

<ParamField body="end" type="int" required>
  The end index of the substring.
</ParamField>

## Response

<ResponseField type="str" required>
  The substring.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.set("key", "Hello World")

  assert redis.getrange("key", 0, 4) == "Hello"
  ```
</RequestExample>
