> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# XPENDING

> Returns information about pending messages in a stream consumer group.

## Arguments

<ParamField body="key" type="str" required>
  The key of the stream.
</ParamField>

<ParamField body="group" type="str" required>
  The consumer group name.
</ParamField>

<ParamField body="start" type="str">
  The minimum pending ID to return (use with end and count).
</ParamField>

<ParamField body="end" type="str">
  The maximum pending ID to return (use with start and count).
</ParamField>

<ParamField body="count" type="int">
  The maximum number of pending messages to return.
</ParamField>

<ParamField body="consumer" type="str">
  Filter results by a specific consumer.
</ParamField>

<ParamField body="idle" type="int">
  Filter by minimum idle time in milliseconds.
</ParamField>

## Response

<ResponseField type="Any">
  When called without range arguments, returns a summary with total count and range info.
  When called with range arguments, returns detailed pending message information.
</ResponseField>

<RequestExample>
  ```py Summary theme={"system"}
  result = redis.xpending("mystream", "mygroup")
  ```

  ```py Detailed with range theme={"system"}
  result = redis.xpending("mystream", "mygroup", start="-", end="+", count=10)
  ```

  ```py Specific consumer with idle filter theme={"system"}
  result = redis.xpending("mystream", "mygroup", start="-", end="+", count=5, consumer="consumer1", idle=10000)
  ```
</RequestExample>

<ResponseExample>
  ```py  theme={"system"}
  [
    2,  # total pending count
    "1638360173533-0",  # smallest pending ID
    "1638360173533-1",  # greatest pending ID
    [["consumer1", "2"]]  # consumers and their pending counts
  ]
  ```
</ResponseExample>
