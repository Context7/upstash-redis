> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# RPUSH

> Push an element at the end of the list.

## Arguments

<ParamField body="key" type="str" required>
  The key of the list.
</ParamField>

<ParamField body="elements" type="*List[str]" required>
  One or more elements to push at the end of the list.
</ParamField>

## Response

<ResponseField type="int" required>
  The length of the list after the push operation.
</ResponseField>

<RequestExample>
  ```py Example  theme={"system"}
  assert redis.rpush("mylist", "one", "two", "three") == 3

  assert lrange("mylist", 0, -1) == ["one", "two", "three"]
  ```
</RequestExample>
