> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# DEL

> Removes the specified keys. A key is ignored if it does not exist.

## Arguments

<ParamField body="keys" type="...string[]" required>
  One or more keys to remove.
</ParamField>

## Response

<ResponseField type="integer" required>
  The number of keys that were removed.
</ResponseField>

<RequestExample>
  ```ts Basic theme={"system"}
  await redis.del("key1", "key2");
  ```

  ```ts Array theme={"system"}
  // in case you have an array of keys
  const keys = ["key1", "key2"];
  await redis.del(...keys)

  ```
</RequestExample>
