> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# FLUSHDB

<Warning>
  Deletes all keys permanently. Use with caution!
</Warning>

## Arguments

<ParamField body="async" type="boolean">
  Whether to perform the operation asynchronously.
  Defaults to synchronous.
</ParamField>

<RequestExample>
  ```ts Sync theme={"system"}
  await redis.flushdb();
  ```

  ```ts Async theme={"system"}
  await redis.flushdb({async: true})
  ```
</RequestExample>
