> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# JSON.ARRTRIM

> Trim an array so that it contains only the specified inclusive range of elements.

## Arguments

<ParamField body="key" type="string" required>
  The key of the json entry.
</ParamField>

<ParamField body="path" type="string" required>
  The path of the array. `$` is the root.
</ParamField>

<ParamField body="start" type="integer" required>
  The start index of the range.
</ParamField>

<ParamField body="stop" type="integer" required>
  The stop index of the range.
</ParamField>

## Response

<ResponseField type="integer[]" required>
  The length of the array after the trimming.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  const length = await redis.json.arrtrim("key", "$.path.to.array", 2, 10);
  ```
</RequestExample>
