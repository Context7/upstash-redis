> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# SCRIPT FLUSH

> Removes all scripts from the script cache.

## Arguments

<ParamField body="flush_type" type="&#x22;ASYNC&#x22; | &#x22;SYNC&#x22;" required>
  Whether to perform the flush asynchronously or synchronously.
</ParamField>

<RequestExample>
  ```py Example theme={"system"}
  redis.script_flush(flush_type="ASYNC")
  ```
</RequestExample>
