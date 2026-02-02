> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# PING

> Send a ping to the server and get a response if the server is alive.

## Arguments

No arguments

## Response

<ResponseField type="str" required>
  `PONG`
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  assert redis.ping() == "PONG"
  ```
</RequestExample>
