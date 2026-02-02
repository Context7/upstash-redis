> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# JSON.STRAPPEND

> Append the json-string values to the string at path.

## Arguments

<ParamField body="key" type="string" required>
  The key of the json entry.
</ParamField>

<ParamField body="path" type="string" required>
  The path of the value. `$` is the root.
</ParamField>

<ParamField body="value" type="string" required>
  The value to append to the existing string.
</ParamField>

## Response

<ResponseField type="integer[]" required>
  The length of the array after the appending.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  await redis.json.strappend("key", "$.path.to.str", "abc");
  ```
</RequestExample>
