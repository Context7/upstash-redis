> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# XREAD

> Reads data from one or multiple streams, starting from the specified IDs.

## Arguments

<ParamField body="key" type="string | string[]" required>
  The key(s) of the stream(s). Can be a single stream key or an array of stream keys.
</ParamField>

<ParamField body="id" type="string | string[]" required>
  The stream entry ID(s) to start reading from. Must match the number of keys provided.
  Use `$` to read only new messages added after the command is issued.
</ParamField>

<ParamField body="options">
  <Expandable title="properties">
    <ParamField body="count" type="number">
      The maximum number of messages to return per stream.
    </ParamField>
  </Expandable>
</ParamField>

## Response

<ResponseField type="Array<[string, Array<[string, string[]]>]> | null">
  Returns an array where each element represents a stream and contains:

  * The stream key
  * An array of messages (ID and field-value pairs)

  Returns null if no data is available.
</ResponseField>

<RequestExample>
  ```ts Single stream theme={"system"}
  const result = await redis.xread("mystream", "0-0");
  ```

  ```ts Multiple streams theme={"system"}
  const result = await redis.xread(
    ["stream1", "stream2"], 
    ["0-0", "0-0"]
  );
  ```

  ```ts With count limit theme={"system"}
  const result = await redis.xread("mystream", "0-0", { count: 2 });
  ```

  ```ts Only new messages theme={"system"}
  const result = await redis.xread("mystream", `$`);
  ```
</RequestExample>

<ResponseExample>
  ```ts  theme={"system"}
  [
    ["mystream", [
      ["1638360173533-0", ["field1", "value1", "field2", "value2"]],
      ["1638360173533-1", ["field1", "value3", "field2", "value4"]]
    ]]
  ]
  ```
</ResponseExample>
