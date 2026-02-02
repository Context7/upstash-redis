> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# ZREVRANK

> Returns the rank of a member in a sorted set, with scores ordered from high to low.

## Arguments

<ParamField body="key" type="string" required>
  The key to get.
</ParamField>

<ParamField body="member" type="TMember" required>
  The member to get the reverse rank of.
</ParamField>

## Response

<ResponseField type="integer" required>
  The reverse rank of the member.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  const rank = await redis.rank("key", "member");
  ```
</RequestExample>
