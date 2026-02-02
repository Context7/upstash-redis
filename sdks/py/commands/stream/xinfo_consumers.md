> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# XINFO CONSUMERS

> List all consumers in a consumer group.

## Arguments

<ParamField body="key" type="str" required>
  The key of the stream.
</ParamField>

<ParamField body="group" type="str" required>
  The consumer group name.
</ParamField>

## Response

<ResponseField type="List[List[Any]]">
  Returns a list of consumer information. Each consumer is represented as a list of key-value pairs.
</ResponseField>

<RequestExample>
  ```py Get consumers info theme={"system"}
  result = redis.xinfo_consumers("mystream", "mygroup")
  ```
</RequestExample>

<ResponseExample>
  ```py  theme={"system"}
  [
    ["name", "consumer1", "pending", 0, "idle", 1000, "inactive", 1000],
    ["name", "consumer2", "pending", 2, "idle", 2000, "inactive", 2000]
  ]
  ```
</ResponseExample>
