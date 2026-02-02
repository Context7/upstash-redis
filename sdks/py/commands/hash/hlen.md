> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# HLEN

> Returns the number of fields contained in the hash stored at key.

## Arguments

<ParamField body="key" type="str" required>
  The key of the hash.
</ParamField>

## Response

<ResponseField type="int" required>
  How many fields are in the hash.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  assert redis.hlen("myhash") == 0

  redis.hset("myhash", values={
      "field1": "Hello",
      "field2": "World"
  })

  assert redis.hlen("myhash") == 2
  ```
</RequestExample>
