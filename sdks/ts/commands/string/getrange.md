> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# GETRANGE

> Return a substring of value at the specified key.

## Arguments

<ParamField body="key" type="string" required>
  The key to get.
</ParamField>

<ParamField body="start" type="integer" required>
  The start index of the substring.
</ParamField>

<ParamField body="end" type="integer" required>
  The end index of the substring.
</ParamField>

## Response

<ResponseField type="string" required>
  The substring.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  const substring = await redis.getrange("key", 2, 4);
  ```
</RequestExample>
