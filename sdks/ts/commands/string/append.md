> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# APPEND

> Append a value to a string stored at key.

## Arguments

<ParamField body="key" type="string" required>
  The key to get.
</ParamField>

<ParamField body="value" required>
  The value to append.
</ParamField>

## Response

<ResponseField type="integer" required>
  How many characters were added to the string.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  await redis.append(key, "Hello");
  // returns 5
  ```
</RequestExample>
