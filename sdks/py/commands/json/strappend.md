> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# JSON.STRAPPEND

> Append the json-string values to the string at path.

## Arguments

<ParamField body="key" type="str" required>
  The key of the json entry.
</ParamField>

<ParamField body="path" type="str" required>
  The path of the string.
</ParamField>

<ParamField body="value" type="str" required>
  The value to append to the existing string.
</ParamField>

## Response

<ResponseField type="List[int]" required>
  The length of the string after the appending.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.json.strappend("key", "$.path.to.str", "abc")
  ```
</RequestExample>
