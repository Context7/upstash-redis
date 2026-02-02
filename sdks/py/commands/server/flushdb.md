> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# FLUSHDB

<Warning>
  Deletes all keys permanently. Use with caution!
</Warning>

## Arguments

<ParamField body="flush_type" type="&#x22;ASYNC&#x22; | &#x22;SYNC&#x22;">
  Whether to perform the operation asynchronously.
  Defaults to synchronous.
</ParamField>

<RequestExample>
  ```py Sync theme={"system"}
  redis.flushall()
  ```

  ```py Async theme={"system"}
  redis.flushall(flush_type="ASYNC")
  ```
</RequestExample>
