> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# ZRANGE

> Returns the specified range of elements in the sorted set stored at key.

## Arguments

<ParamField body="key" type="str" required>
  The key to get.
</ParamField>

<ParamField body="min" type="float | str" required>
  The minimum value to include.
</ParamField>

<ParamField body="max" type="float | str" required>
  The maximum value to include.
</ParamField>

"-inf" and "+inf" are also valid values for the ranges

<ParamField body="withscores" type="bool">
  Whether to include the scores in the response.
</ParamField>

<ParamField body="rev" type="bool">
  Whether to reverse the order of the response.
</ParamField>

<ParamField body="sortby" type="&#x22;BYSCORE&#x22; | &#x22;BYLEX&#x22;">
  If bylex
</ParamField>

<ParamField body="offset" type="int">
  The offset to start from.
</ParamField>

<ParamField body="count" type="int">
  The number of elements to return.
</ParamField>

## Response

<ResponseField type="List[str] | List[Tuple[str, float]]">
  The values in the specified range.

  If `withscores` is true, the members will be tuples of the form `(member, score)`.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.zadd("myset", {"a": 1, "b": 2, "c": 3})

  assert redis.zrange("myset", 0, 1) == ["a", "b"]
  ```

  ```py Reverse theme={"system"}
  redis.zadd("myset", {"a": 1, "b": 2, "c": 3})

  assert redis.zrange("myset", 0, 1, rev=True) == ["c", "b"]

  ```

  ```py Sorted theme={"system"}
  redis.zadd("myset", {"a": 1, "b": 2, "c": 3})

  assert redis.zrange("myset", 0, 1, sortby="BYSCORE") == ["a", "b"]

  ```

  ```py With scores theme={"system"}
  redis.zadd("myset", {"a": 1, "b": 2, "c": 3})

  assert redis.zrange("myset", 0, 1, withscores=True) == [("a", 1), ("b", 2)]
  ```
</RequestExample>
