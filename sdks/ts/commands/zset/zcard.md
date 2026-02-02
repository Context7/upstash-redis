> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# ZCARD

> Returns the number of elements in the sorted set stored at key.

## Arguments

<ParamField body="key" type="string" required>
  The key to get.
</ParamField>

## Response

<ResponseField type="integer" required>
  The number of elements in the sorted set.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}

  await redis.zadd("key", 
      { score: 1, member: "one"}, 
      { score: 2, member: "two" },
  );
  const elements = await redis.zrank("key");
  console.log(elements); // 2
  ```
</RequestExample>
