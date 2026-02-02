> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# UNLINK

> Removes the specified keys. A key is ignored if it does not exist.

## Arguments

<ParamField body="keys" type="...string[]" required>
  One or more keys to unlink.
</ParamField>

## Response

<ResponseField type="integer" required>
  The number of keys that were unlinked.
</ResponseField>

<RequestExample>
  ```ts Basic theme={"system"}
  await redis.unlink("key1", "key2");
  ```

  ```ts Array theme={"system"}
  // in case you have an array of keys
  const keys = ["key1", "key2"];
  await redis.unlink(...keys)

  ```
</RequestExample>
