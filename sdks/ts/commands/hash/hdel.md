> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# HDEL

> Deletes one or more hash fields.

## Arguments

<ParamField body="key" type="string" required>
  The key to get.
</ParamField>

<ParamField body="fields" required>
  One or more fields to delete.
</ParamField>

## Response

<ResponseField type="integer" required>
  The number of fields that were removed from the hash.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  await redis.hdel(key, 'field1', 'field2');
  // returns 5
  ```
</RequestExample>
