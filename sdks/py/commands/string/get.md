> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# GET

> Return the value of the specified key or `None` if the key doesn't exist.

## Arguments

<ParamField body="key" type="str" required>
  The key to get.
</ParamField>

## Response

<ResponseField required>
  The response is the value stored at the key or `None` if the key doesn't exist.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.set("key", "value")

  assert redis.get("key") == "value"
  ```
</RequestExample>
