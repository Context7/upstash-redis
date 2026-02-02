> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# FUNCTION DELETE

> Delete a library and all its functions.

## Arguments

<ParamField body="libraryName" type="string" required>
  The name of the library to delete.
</ParamField>

## Response

<ResponseField type="string" required>
  "OK"
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  await redis.functions.delete("mylib")
  ```
</RequestExample>
