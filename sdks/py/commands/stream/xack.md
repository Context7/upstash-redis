> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# XACK

> Removes one or multiple messages from the pending entries list of a stream consumer group.

## Arguments

<ParamField body="key" type="str" required>
  The key of the stream.
</ParamField>

<ParamField body="group" type="str" required>
  The consumer group name.
</ParamField>

<ParamField body="ids" type="str" required>
  The ID(s) of the message(s) to acknowledge. Can be multiple IDs as separate arguments.
</ParamField>

## Response

<ResponseField type="int">
  The number of messages successfully acknowledged.
</ResponseField>

<RequestExample>
  ```py Single message theme={"system"}
  result = redis.xack("mystream", "mygroup", "1638360173533-0")
  ```

  ```py Multiple messages theme={"system"}
  result = redis.xack("mystream", "mygroup", "1638360173533-0", "1638360173533-1")
  ```
</RequestExample>
