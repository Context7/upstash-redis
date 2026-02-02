> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# JSON.OBJKEYS

> Return the keys in the object that`s referenced by path.

## Arguments

<ParamField body="key" type="str" required>
  The key of the json entry.
</ParamField>

<ParamField body="path" type="str" required>
  The path of the object. `$` is the root.
</ParamField>

## Response

<ResponseField type="List[List[str]]" required>
  The keys of the object at the path.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  keys = redis.json.objkeys("key", "$.path")
  ```
</RequestExample>
