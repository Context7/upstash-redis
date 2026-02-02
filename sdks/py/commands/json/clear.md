> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# JSON.CLEAR

> Clear container values (arrays/objects) and set numeric values to 0.

## Arguments

<ParamField body="key" type="str" required>
  The key of the json entry.
</ParamField>

<ParamField body="path" type="str" required>
  The path to clear. `$` is the root.
</ParamField>

## Response

<ResponseField type="List[int]" required>
  How many keys cleared from the objects.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.json.clear("key")
  ```

  ```py With path theme={"system"}
  redis.json.clear("key", "$.my.key")
  ```
</RequestExample>
