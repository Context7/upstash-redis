> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# SCRIPT EXISTS

> Check if scripts exist in the script cache.

## Arguments

<ParamField body="hashes" type="string[]" required>
  The sha1 of the scripts to check.
</ParamField>

## Response

<ResponseField type="number[]" required>
  An array of numbers. `1` if the script exists, otherwise `0`.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  await redis.scriptExists("<sha1>", "<sha2>")

  // Returns 1 
  // [1, 0]
  ```
</RequestExample>
