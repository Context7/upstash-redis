> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# JSON.NUMMULTBY

> Multiply the number value stored at `path` by number.

## Arguments

<ParamField body="key" type="str" required>
  The key of the json entry.
</ParamField>

<ParamField body="path" type="str" required>
  The path of the number.
</ParamField>

<ParamField body="multiply" type="number" required>
  The number to multiply by.
</ParamField>

## Response

<ResponseField type="List[int]" required>
  The new value after multiplying
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  newValue = redis.json.nummultby("key", "$.path.to.value", 2)
  ```
</RequestExample>
