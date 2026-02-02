> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# RENAME

> Rename a key

## Arguments

<ParamField body="source" type="string" required>
  The original key.
</ParamField>

<ParamField body="destination" type="string" required>
  A new name for the key.
</ParamField>

## Response

<ResponseField type="string" required>
  `OK`
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
   await redis.rename("old", "new");
  ```
</RequestExample>
