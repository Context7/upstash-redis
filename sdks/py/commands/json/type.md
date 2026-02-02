> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# JSON.TYPE

> Report the type of JSON value at `path`.

## Arguments

<ParamField body="key" type="str" required>
  The key of the json entry.
</ParamField>

<ParamField body="path" type="str" required>
  The path of the value. `$` is the root.
</ParamField>

## Response

<ResponseField type="List[str | null]" required>
  The type of the value at `path` or `null` if the value does not exist.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  myType = redis.json.type("key", "$.path.to.value")
  ```
</RequestExample>
