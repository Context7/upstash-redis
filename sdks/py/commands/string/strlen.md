> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# STRLEN

> Return the length of a string stored at a key.

The \`STRLEN\`\` command in Redis is used to find the length of the string value associated with a key. In Redis, keys can be associated with various data types, and one of these data types is the "string." The STRLEN command specifically operates on keys that are associated with string values.

## Arguments

<ParamField body="key" type="str" required>
  The name of the Redis key.
</ParamField>

## Response

<ResponseField type="int" required>
  The length of the value.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.set("key", "Hello World")

  assert redis.strlen("key") == 11
  ```
</RequestExample>
