> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# XGROUP DESTROY

> Delete an entire consumer group.

## Arguments

<ParamField body="key" type="str" required>
  The key of the stream.
</ParamField>

<ParamField body="group" type="str" required>
  The consumer group name to destroy.
</ParamField>

## Response

<ResponseField type="int">
  Returns 1 if the group was destroyed, 0 if it didn't exist.
</ResponseField>

<RequestExample>
  ```py Destroy existing group theme={"system"}
  result = redis.xgroup_destroy("mystream", "mygroup")
  ```
</RequestExample>
