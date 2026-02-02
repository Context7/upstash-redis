> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# LSET

> Set a value at a specific index.

## Arguments

<ParamField body="key" type="str" required>
  The key of the list.
</ParamField>

<ParamField body="index" type="number" required>
  At which index to set the value.
</ParamField>

<ParamField body="element" type="str" required>
  The value to set.
</ParamField>

## Response

<ResponseField type="bool" required>
  Returns `True` if the index was in range and the value was set.
</ResponseField>

<RequestExample>
  ```py Example  theme={"system"}
  redis.rpush("mylist", "one", "two", "three")

  assert redis.lset("mylist", 1, "Hello") == True

  assert redis.lrange("mylist", 0, -1) == ["one", "Hello", "three"]

  assert redis.lset("mylist", 5, "Hello") == False

  assert redis.lrange("mylist", 0, -1) == ["one", "Hello", "three"]
  ```
</RequestExample>
