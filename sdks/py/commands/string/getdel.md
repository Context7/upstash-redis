> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# GETDEL

> Return the value of the specified key and delete the key.

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

  assert redis.getdel("key") == "value"

  assert redis.get("key") == None
  ```
</RequestExample>
