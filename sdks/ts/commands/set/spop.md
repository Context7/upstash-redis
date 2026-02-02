> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# SPOP

> Removes and returns one or more random members from a set.

## Arguments

<ParamField body="key" type="string" required>
  The key of the set.
</ParamField>

<ParamField body="count" type="number" default={1}>
  How many members to remove and return.
</ParamField>

## Response

<ResponseField type="TMember | TMember[]" required>
  The popped member.
  If `count` is specified, an array of members is returned.
</ResponseField>

<RequestExample>
  ```ts Example  theme={"system"}
  await redis.sadd("set", "a", "b", "c"); 
  const popped = await redis.spop("set");
  console.log(popped); // "a"
  ```

  ```ts With Count  theme={"system"}
  await redis.sadd("set", "a", "b", "c"); 
  const popped = await redis.spop("set", 2);
  console.log(popped); // ["a", "b"]
  ```
</RequestExample>
