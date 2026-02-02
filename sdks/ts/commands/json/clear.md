> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# JSON.CLEAR

> Clear container values (arrays/objects) and set numeric values to 0.

## Arguments

<ParamField body="key" type="string" required>
  The key of the json entry.
</ParamField>

<ParamField body="path" type="string" required>
  The path to clear. `$` is the root.
</ParamField>

## Response

<ResponseField type="integer[]" required>
  How many values were cleared.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  await redis.json.clear("key");
  ```

  ```ts With path theme={"system"}
  await redis.json.clear("key", "$.my.key");
  ```
</RequestExample>
