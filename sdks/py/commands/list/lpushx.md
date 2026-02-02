> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# LPUSHX

> Push an element at the head of the list only if the list exists.

## Arguments

<ParamField body="key" type="str" required>
  The key of the list.
</ParamField>

<ParamField body="elements" type="*List[str]" required>
  One or more elements to push at the head of the list.
</ParamField>

## Response

<ResponseField type="number" required>
  The length of the list after the push operation.

  `0` if the list did not exist and thus no element was pushed.
</ResponseField>

<RequestExample>
  ```py Example  theme={"system"}
  # Initialize the list
  redis.lpush("mylist", "one")

  assert redis.lpushx("mylist", "two", "three") == 3

  assert lrange("mylist", 0, -1) == ["three", "two", "one"]

  # Non existing key
  assert redis.lpushx("non-existent-list", "one") == 0
  ```
</RequestExample>
