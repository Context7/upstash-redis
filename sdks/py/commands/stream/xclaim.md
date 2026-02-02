> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# XCLAIM

> Changes the ownership of pending messages from one consumer to another in a stream consumer group.

## Arguments

<ParamField body="key" type="str" required>
  The key of the stream.
</ParamField>

<ParamField body="group" type="str" required>
  The consumer group name.
</ParamField>

<ParamField body="consumer" type="str" required>
  The consumer name that will claim the messages.
</ParamField>

<ParamField body="min_idle_time" type="int" required>
  The minimum idle time in milliseconds for messages to be claimed.
</ParamField>

<ParamField body="ids" type="str" required>
  The ID(s) of the message(s) to claim. Can be multiple IDs as separate arguments.
</ParamField>

<ParamField body="justid" type="bool">
  Return only the message IDs instead of the full message data.
</ParamField>

## Response

<ResponseField type="Union[List[List[Any]], List[str]]">
  Returns a list of claimed messages. If `justid` option is used, returns only message IDs.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  # Claim messages that have been idle for more than 60 seconds
  result = redis.xclaim(
      "mystream",
      "mygroup",
      "consumer1",
      60000,  # 60 seconds
      "1638360173533-0", "1638360173533-1"
  )
  ```

  ```py With justid option theme={"system"}
  result = redis.xclaim(
      "mystream",
      "mygroup", 
      "consumer1",
      60000,
      "1638360173533-0",
      justid=True
  )
  ```
</RequestExample>

<ResponseExample>
  ```py  theme={"system"}
  [
    ["1638360173533-0", ["field1", "value1", "field2", "value2"]],
    ["1638360173533-1", ["field1", "value3", "field2", "value4"]]
  ]
  ```
</ResponseExample>
