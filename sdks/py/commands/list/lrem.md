> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# LREM

> Remove the first `count` occurrences of an element from a list.

## Arguments

<ParamField body="key" type="str" required>
  The key of the list.
</ParamField>

<ParamField body="count" type="number" required>
  How many occurrences of the element to remove.
</ParamField>

<ParamField body="element" type="Any" required>
  The element to remove
</ParamField>

## Response

<ResponseField type="int" required>
  The number of elements removed.
</ResponseField>

<RequestExample>
  ```py Example  theme={"system"}
  redis.rpush("mylist", "one", "two", "three", "two", "one")

  assert redis.lrem("mylist", 2, "two") == 2

  assert redis.lrange("mylist", 0, -1) == ["one", "three", "one"]
  ```
</RequestExample>
