> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# ECHO

Returns a message back to you. Useful for debugging the connection.

## Arguments

<ParamField body="message" type="string" required>
  A message to send to the server.
</ParamField>

## Response

<ResponseField type="string" required>
  The same message you sent.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  const response = await redis.echo("hello world");
  console.log(response); // "hello world"
  ```
</RequestExample>
