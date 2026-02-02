> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# KEYS

> Returns all keys matching pattern.

<Warning>
  This command can block the database for an extended period, especially with large datasets. We recommend using [SCAN](/redis/sdks/py/commands/generic/scan) instead for production environments.

  This command will return an error for databases containing more than 100,000 entries.
</Warning>

## Arguments

<ParamField body="match" type="str" required>
  A glob-style pattern. Use `*` to match all keys.
</ParamField>

## Response

<ResponseField type="List[str]">
  Array of keys matching the pattern.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  keys = redis.keys("prefix*")
  ```

  ```py Match All theme={"system"}
  keys = redis.keys("*")
  ```
</RequestExample>
