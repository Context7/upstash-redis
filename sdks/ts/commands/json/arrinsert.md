> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# JSON.ARRINSERT

> Insert the json values into the array at path before the index (shifts to the right).

## Arguments

<ParamField body="key" type="string" required>
  The key of the json entry.
</ParamField>

<ParamField body="path" type="string" required>
  The path of the array. `$` is the root.
</ParamField>

<ParamField body="index" type="integer" required>
  The index where to insert the values.
</ParamField>

<ParamField body="values" type="...TValue[]" required>
  One or more values to append to the array.
</ParamField>

## Response

<ResponseField type="integer[]" required>
  The length of the array after the insertion.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  const length = await redis.json.arrinsert("key", "$.path.to.array", 2, "a", "b");
  ```
</RequestExample>
