> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# XINFO GROUPS

> List all consumer groups for a stream.

## Arguments

<ParamField body="key" type="str" required>
  The key of the stream.
</ParamField>

## Response

<ResponseField type="List[List[Any]]">
  Returns a list of consumer group information. Each group is represented as a list of key-value pairs.
</ResponseField>

<RequestExample>
  ```py Get groups info theme={"system"}
  result = redis.xinfo_groups("mystream")
  ```
</RequestExample>

<ResponseExample>
  ```py  theme={"system"}
  [
    ["name", "group1", "consumers", 2, "pending", 0, "last-delivered-id", "1638360173533-0"],
    ["name", "group2", "consumers", 0, "pending", 3, "last-delivered-id", "0-0"]
  ]
  ```
</ResponseExample>
