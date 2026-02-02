> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# XGROUP DELCONSUMER

> Delete a consumer from a consumer group.

## Arguments

<ParamField body="key" type="str" required>
  The key of the stream.
</ParamField>

<ParamField body="group" type="str" required>
  The consumer group name.
</ParamField>

<ParamField body="consumer" type="str" required>
  The consumer name to delete.
</ParamField>

## Response

<ResponseField type="int">
  Returns the number of pending messages the consumer had.
</ResponseField>

<RequestExample>
  ```py Delete existing consumer theme={"system"}
  result = redis.xgroup_delconsumer("mystream", "mygroup", "consumer1")
  ```
</RequestExample>
