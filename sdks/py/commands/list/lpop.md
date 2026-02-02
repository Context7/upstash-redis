> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# LPOP

> Remove and return the first element(s) of a list

## Arguments

<ParamField body="key" type="str" required>
  The key of the list.
</ParamField>

<ParamField body="count" type="int">
  How many elements to pop. If not specified, a single element is popped.
</ParamField>

## Response

<ResponseField type="str | List[str] None" required>
  The popped element(s). If `count` was specified, an array of elements is
  returned, otherwise a single element is returned. If the list is empty, `None`
  is returned.
</ResponseField>

<RequestExample>
  ```py Single  theme={"system"}
  redis.rpush("mylist", "one", "two", "three")

  assert redis.lpop("mylist") == "one"
  ```

  ```py Multiple theme={"system"}
  redis.rpush("mylist", "one", "two", "three")

  assert redis.lpop("mylist", 2) == ["one", "two"]
  ```
</RequestExample>
