> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# JSON.MSET

> Sets multiple JSON values at multiple paths in multiple keys.

## Arguments

<ParamField body="key_path_value_tuples" type="List[Tuple[string, string, TValue]]" required>
  A list of tuples where each tuple contains a key, a path, and a value.
</ParamField>

## Response

<ResponseField type="true" required>
  Returns true if the operation was successful.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.json.mset([(key, "$.path", value), (key2, "$.path2", value2)])
  ```
</RequestExample>
