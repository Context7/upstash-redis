> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# MSET

> Set multiple keys in one go.

For billing purposes, this counts as a single command.

## Arguments

<ParamField type="Dict[str, Any]" required>
  An object where the keys are the keys to set, and the values are the values to set.
</ParamField>

## Response

<ResponseField type="bool" required>
  `True` if the operation succeeded.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.mset({
    "key1": "value1",
    "key2": "value2"
  })
  ```
</RequestExample>
