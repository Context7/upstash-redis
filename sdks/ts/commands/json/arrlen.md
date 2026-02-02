> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# JSON.ARRLEN

> Report the length of the JSON array at `path` in `key`.

## Arguments

<ParamField body="key" type="string" required>
  The key of the json entry.
</ParamField>

<ParamField body="path" type="string" required>
  The path of the array. `$` is the root.
</ParamField>

## Response

<ResponseField type="integer[]" required>
  The length of the array.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  const length = await redis.json.arrlen("key", "$.path.to.array");
  ```
</RequestExample>
