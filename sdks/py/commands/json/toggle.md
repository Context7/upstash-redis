> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# JSON.TOGGLE

> Toggle a boolean value stored at `path`.

## Arguments

<ParamField body="key" type="str" required>
  The key of the json entry.
</ParamField>

<ParamField body="path" type="str" required>
  The path of the boolean. `$` is the root.
</ParamField>

## Response

<ResponseField type="List[boolean]" required>
  The new value of the boolean.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  bool = redis.json.toggle("key", "$.path.to.bool")
  ```
</RequestExample>
