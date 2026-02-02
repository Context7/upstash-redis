> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# JSON.DEL

> Delete a key from a JSON document.

## Arguments

<ParamField body="key" type="str" required>
  The key of the json entry.
</ParamField>

<ParamField body="path" type="str" required>
  The path to delete. `$` is the root.
</ParamField>

## Response

<ResponseField type="int" required>
  How many paths were deleted.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.json.del("key", "$.path.to.value")
  ```
</RequestExample>
