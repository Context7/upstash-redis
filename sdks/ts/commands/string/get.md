> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# GET

> Return the value of the specified key or `null` if the key doesn't exist.

## Arguments

<ParamField body="key" type="string" required>
  The key to get.
</ParamField>

## Response

<ResponseField required>
  The response is the value stored at the key or `null` if the key doesn't exist.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  type MyType = {
      a: number;
      b: string;
  }
  const value = await redis.get<MyType>("key");
  if (!value) {
      // key doesn't exist
  } else {
      // value is of type MyType
  }
  ```
</RequestExample>
