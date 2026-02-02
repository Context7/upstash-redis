> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# XRANGE

> Returns stream entries matching a given range of IDs.

## Arguments

<ParamField body="key" type="str" required>
  The key of the stream.
</ParamField>

<ParamField body="start" type="str" default="-">
  The stream entry ID to start from. Use "-" for the first available ID.
</ParamField>

<ParamField body="end" type="str" default="+">
  The stream entry ID to end at. Use "+" for the last available ID.
</ParamField>

<ParamField body="count" type="int">
  The maximum number of entries to return.
</ParamField>

## Response

<ResponseField type="List[Tuple[str, List[str]]]">
  A list of stream entries, where each entry is a tuple containing the stream ID and its associated fields and values.
</ResponseField>

<RequestExample>
  ```py All entries theme={"system"}
  result = redis.xrange("mystream", "-", "+")
  ```

  ```py Range with specific IDs theme={"system"}
  result = redis.xrange("mystream", "1548149259438-0", "1548149259438-5")
  ```

  ```py Limited count theme={"system"}
  result = redis.xrange("mystream", "-", "+", count=10)
  ```
</RequestExample>

<ResponseExample>
  ```py  theme={"system"}
  {
    "1548149259438-0": {
      "field1": "value1",
      "field2": "value2"
    },
    "1548149259438-1": {
      "field1": "value3",
      "field2": "value4"
    }
  }
  ```
</ResponseExample>
