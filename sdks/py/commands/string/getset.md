> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# GETSET

> Return the value of the specified key and replace it with a new value.

## Arguments

<ParamField body="key" type="str" required>
  The key to get.
</ParamField>

<ParamField body="value" type="Any" required>
  The new value to store.
</ParamField>

## Response

<ResponseField required>
  The response is the value stored at the key or `None` if the key doesn't exist.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.set("key", "old-value")

  assert redis.getset("key", "newvalue") == "old-value"
  ```
</RequestExample>
