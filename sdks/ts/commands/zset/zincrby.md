> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# ZINCRBY

> Increment the score of a member.

## Arguments

<ParamField body="key" type="string" required>
  The key of the sorted set.
</ParamField>

<ParamField body="increment" type="integer" required>
  The increment to add to the score.
</ParamField>

<ParamField body="member" type="TMember" required>
  The member to increment.
</ParamField>

## Response

<ResponseField type="integer" required>
  The new score of `member` after the increment operation.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  await redis.zadd("key", 1, "member");
  const value = await redis.zincrby("key", 2, "member");
  console.log(value); // 3
  ```
</RequestExample>
