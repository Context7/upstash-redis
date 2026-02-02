> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# LINDEX

> Returns the element at index index in the list stored at key.

The index is zero-based, so 0 means the first element, 1 the second element and so on. Negative indices can be used to designate elements starting at the tail of the list.

## Arguments

<ParamField body="key" type="str" required>
  The key of the list.
</ParamField>

<ParamField body="index" type="int" required>
  The index of the element to return, zero-based.
</ParamField>

## Response

<ResponseField type="Optional[str]" required>
  The value of the element at index index in the list. If the index is out of range, `None` is returned.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.rpush("key", "a", "b", "c")

  assert redis.lindex("key", 0) == "a"
  ```
</RequestExample>
