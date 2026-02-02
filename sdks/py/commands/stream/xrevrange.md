> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# XREVRANGE

> Returns stream entries matching a given range of IDs in reverse order.

## Arguments

<ParamField body="key" type="str" required>
  The key of the stream.
</ParamField>

<ParamField body="end" type="str" default="+">
  The stream entry ID to end at (highest ID).
</ParamField>

<ParamField body="start" type="str" default="-">
  The stream entry ID to start from (lowest ID).
</ParamField>

<ParamField body="count" type="int">
  The maximum number of entries to return.
</ParamField>

## Response

<ResponseField type="List[List[Any]]">
  Returns a list of stream entries in reverse chronological order. Each entry contains the ID and field-value pairs.
</ResponseField>

<RequestExample>
  ```py All entries (reverse order) theme={"system"}
  result = redis.xrevrange("mystream", "+", "-")
  ```

  ```py Limited count theme={"system"}
  result = redis.xrevrange("mystream", "+", "-", count=2)
  ```

  ```py Specific range theme={"system"}
  result = redis.xrevrange("mystream", end="1638360173533-2", start="1638360173533-0")
  ```
</RequestExample>

<ResponseExample>
  ```py  theme={"system"}
  [
    ["1638360173533-2", ["field1", "value5", "field2", "value6"]],
    ["1638360173533-1", ["field1", "value3", "field2", "value4"]],
    ["1638360173533-0", ["field1", "value1", "field2", "value2"]]
  ]
  ```
</ResponseExample>
