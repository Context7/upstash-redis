> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# ZLEXCOUNT

> Returns the number of elements in the sorted set stored at key filterd by lex.

## Arguments

<ParamField body="key" type="str" required>
  The key to get.
</ParamField>

<ParamField body="min" type="str" required>
  The lower lexicographical bound to filter by.

  Use `-` to disable the lower bound.
</ParamField>

<ParamField body="max" type="str" required>
  The upper lexicographical bound to filter by.

  Use `+` to disable the upper bound.
</ParamField>

## Response

<ResponseField type="int" required>
  The number of matched.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.zadd("myset", {"a": 1, "b": 2, "c": 3})

  assert redis.zlexcount("myset", "-", "+") == 3
  ```
</RequestExample>
