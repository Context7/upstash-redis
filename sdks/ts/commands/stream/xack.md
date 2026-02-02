> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# XACK

> Removes one or multiple messages from the pending entries list of a stream consumer group.

## Arguments

<ParamField body="key" type="string" required>
  The key of the stream.
</ParamField>

<ParamField body="group" type="string" required>
  The consumer group name.
</ParamField>

<ParamField body="id" type="string | string[]" required>
  The ID(s) of the message(s) to acknowledge. Can be a single ID or an array of IDs.
</ParamField>

## Response

<ResponseField type="number">
  The number of messages successfully acknowledged.
</ResponseField>

<RequestExample>
  ```ts Single message theme={"system"}
  const result = await redis.xack("mystream", "mygroup", "1638360173533-0");
  ```

  ```ts Multiple messages theme={"system"}
  const result = await redis.xack("mystream", "mygroup", [
    "1638360173533-0",
    "1638360173533-1"
  ]);
  ```
</RequestExample>
