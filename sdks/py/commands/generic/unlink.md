> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# UNLINK

> Removes the specified keys. A key is ignored if it does not exist.

## Arguments

<ParamField body="keys" type="*List[str]" required>
  One or more keys to unlink.
</ParamField>

## Response

<ResponseField type="int" required>
  The number of keys that were unlinked.
</ResponseField>

<RequestExample>
  ```py Basic theme={"system"}
  assert redis.unlink("key1", "key2", "key3") == 3
  ```
</RequestExample>
