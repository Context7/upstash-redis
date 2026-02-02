> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# XGROUP CREATE

> Create a new consumer group for a Redis stream.

## Arguments

<ParamField body="key" type="str" required>
  The key of the stream.
</ParamField>

<ParamField body="group" type="str" required>
  The consumer group name.
</ParamField>

<ParamField body="id" type="str" required>
  The stream entry ID to start consuming from. Use '\$' to start from the end.
</ParamField>

<ParamField body="mkstream" type="bool">
  Create the stream if it doesn't exist.
</ParamField>

## Response

<ResponseField type="str">
  Returns "OK" if the consumer group was created successfully.
</ResponseField>

<RequestExample>
  ```py Start from end theme={"system"}
  result = redis.xgroup_create("mystream", "mygroup", "$")
  ```

  ```py Create stream if not exists theme={"system"}
  result = redis.xgroup_create("newstream", "mygroup", "$", mkstream=True)
  ```

  ```py Start from beginning theme={"system"}
  result = redis.xgroup_create("mystream", "mygroup2", "0-0")
  ```
</RequestExample>
