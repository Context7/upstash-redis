> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# RENAMENX

> Rename a key if it does not already exist.

## Arguments

<ParamField body="source" type="string" required>
  The original key.
</ParamField>

<ParamField body="destination" type="string" required>
  A new name for the key.
</ParamField>

## Response

<ResponseField type="0 | 1" required>
  `1` if key was renamed, `0` if key was not renamed.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  const renamed = await redis.renamenx("old", "new");
  ```
</RequestExample>
