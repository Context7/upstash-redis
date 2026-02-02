> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# ZREM

> Remove one or more members from a sorted set

## Arguments

<ParamField body="key" type="string" required>
  The key of the sorted set
</ParamField>

<ParamField body="members" type="...TMember[]" required>
  One or more members to remove
</ParamField>

## Response

<ResponseField required>
  The number of members removed from the sorted set.
</ResponseField>

<RequestExample>
  ```ts Single theme={"system"}
  await redis.zrem("key", "member");
  ```

  ```ts Multiple theme={"system"}
  await redis.zrem("key", "member1", "member2");
  ```
</RequestExample>
