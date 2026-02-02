> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# JSON.MERGE

> Merges the JSON value at path in key with the provided value.

## Arguments

<ParamField body="key" type="str" required>
  The key of the json entry.
</ParamField>

<ParamField body="path" type="str" required>
  The path of the value to set.
</ParamField>

<ParamField body="value" type="TValue" required>
  The value to merge with.
</ParamField>

## Response

<ResponseField type="true" required>
  Returns true if the merge was successful.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.json.merge("key", "$.path.to.value", {"new": "value"})
  ```
</RequestExample>
