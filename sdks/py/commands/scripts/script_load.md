> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# SCRIPT LOAD

> Load the specified Lua script into the script cache.

## Arguments

<ParamField body="script" type="str" required>
  The script to load.
</ParamField>

## Response

<ResponseField type="str" required>
  The sha1 of the script.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  sha1 = redis.script_load("return 1")

  assert redis.evalsha(sha1) == 1
  ```
</RequestExample>
