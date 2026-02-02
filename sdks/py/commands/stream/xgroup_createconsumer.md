> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# XGROUP CREATECONSUMER

> Create a new consumer in an existing consumer group.

## Arguments

<ParamField body="key" type="str" required>
  The key of the stream.
</ParamField>

<ParamField body="group" type="str" required>
  The consumer group name.
</ParamField>

<ParamField body="consumer" type="str" required>
  The consumer name to create.
</ParamField>

## Response

<ResponseField type="int">
  Returns 1 if the consumer was created, 0 if it already existed.
</ResponseField>

<RequestExample>
  ```py Create new consumer theme={"system"}
  result = redis.xgroup_createconsumer("mystream", "mygroup", "consumer1")
  ```
</RequestExample>
