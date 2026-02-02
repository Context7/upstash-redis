> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# JSON.ARRINDEX

> Search for the first occurrence of a JSON value in an array.

## Arguments

<ParamField body="key" type="string" required>
  The key of the json entry.
</ParamField>

<ParamField body="path" type="string" required>
  The path of the array. `$` is the root.
</ParamField>

<ParamField body="value" type="TValue" required>
  The value to search for.
</ParamField>

<ParamField body="start" type="integer" default={0}>
  The start index.
</ParamField>

<ParamField body="stop" type="integer" default={0}>
  The stop index.
</ParamField>

## Response

<ResponseField type="integer[]" required>
  The index of the first occurrence of the value in the array, or -1 if not found.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  const index = await redis.json.arrindex("key", "$.path.to.array", "a");
  ```
</RequestExample>
