> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# ECHO

Returns a message back to you. Useful for debugging the connection.

## Arguments

<ParamField body="message" type="str" required>
  A message to send to the server.
</ParamField>

## Response

<ResponseField type="str" required>
  The same message you sent.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  assert redis.echo("hello world") == "hello world"
  ```
</RequestExample>
