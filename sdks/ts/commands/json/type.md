> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# JSON.TYPE

> Report the type of JSON value at `path`.

## Arguments

<ParamField body="key" type="string" required>
  The key of the json entry.
</ParamField>

<ParamField body="path" type="string" required>
  The path of the value. `$` is the root.
</ParamField>

## Response

<ResponseField type="(string | null)[]" required>
  The type of the value at `path` or `null` if the value does not exist.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  const myType = await redis.json.type("key", "$.path.to.value");
  ```
</RequestExample>
