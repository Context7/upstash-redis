> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# XRANGE

> Returns stream entries matching a given range of IDs.

## Arguments

<ParamField body="key" type="string" required>
  The key to of the stream.
</ParamField>

<ParamField body="start" type="string" required>
  The stream entry ID to start from.
</ParamField>

<ParamField body="end" type="string" required>
  The stream entry ID to end at.
</ParamField>

<ParamField body="count" type="number">
  The maximum number of entries to return.
</ParamField>

## Response

<ResponseField type="Record<streamId, Record<field, value>>">
  An object of stream entries, keyed by their stream ID
</ResponseField>

<RequestExample>
  ```ts All entries theme={"system"}
  const result = await redis.xrange("mystream", "-", "+");
  ```

  ```ts Range with specific IDs theme={"system"}
  const result = await redis.xrange("mystream", "1548149259438-0", "1548149259438-5");
  ```

  ```ts Limited count theme={"system"}
  const result = await redis.xrange("mystream", "-", "+", 10);
  ```
</RequestExample>

<ResponseExample>
  ```ts  theme={"system"}
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
