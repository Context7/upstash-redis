> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# APPEND

> Append a value to a string stored at key.

## Arguments

<ParamField body="key" type="str" required>
  The key to get.
</ParamField>

<ParamField body="value" required>
  The value to append.
</ParamField>

## Response

<ResponseField type="int" required>
  How many characters were added to the string.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.set("key", "Hello")

  assert redis.append("key", " World") == 11

  assert redis.get("key") == "Hello World"
  ```
</RequestExample>
