> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# JSON.OBJKEYS

> Return the keys in the object that`s referenced by path.

## Arguments

<ParamField body="key" type="string" required>
  The key of the json entry.
</ParamField>

<ParamField body="path" type="string" required>
  The path of the array. `$` is the root.
</ParamField>

## Response

<ResponseField type="string[][]" required>
  The keys of the object at the path.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  const keys = await redis.json.objkeys("key", "$.path");
  ```
</RequestExample>
