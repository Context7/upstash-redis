> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# JSON.OBJLEN

> Report the number of keys in the JSON object at `path` in `key`.

## Arguments

<ParamField body="key" type="string" required>
  The key of the json entry.
</ParamField>

<ParamField body="path" type="string" required>
  The path of the object. `$` is the root.
</ParamField>

## Response

<ResponseField type="integer[]" required>
  The number of keys in the objects.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  const lengths = await redis.json.objlen("key", "$.path");
  ```
</RequestExample>
