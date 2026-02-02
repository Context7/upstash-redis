> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# PUBLISH

> Publish a message to a channel

## Arguments

<ParamField body="channel" type="string" required>
  The channel to publish to.
</ParamField>

<ParamField body="message" type="TMessage">
  The message to publish.
</ParamField>

## Response

<ResponseField type="integer" required>
  The number of clients who received the message.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  const listeners = await redis.publish("my-channel", "my-message");
  ```
</RequestExample>
