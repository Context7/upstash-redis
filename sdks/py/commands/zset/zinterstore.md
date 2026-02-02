> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# ZINTERSTORE

> Calculates the intersection of sets and stores the result in a key

## Arguments

<ParamField body="destination" type="str" required>
  The key to store the result in.
</ParamField>

<ParamField body="keys" type="List[str]" required>
  The keys of the sets to compare.
</ParamField>

<ParamField body="weights" type="List[float]" default="None">
  The weights to apply to the sets.
</ParamField>

<ParamField body="aggregate" type="&#x22;SUM&#x22; | &#x22;MIN&#x22; | &#x22;MAX&#x22;" default="sum">
  The aggregation function to apply to the sets.
</ParamField>

<ParamField body="withscores" type="bool" default="false">
  Whether to include scores in the result.
</ParamField>

## Response

## Response

<ResponseField required>
  The number of elements in the resulting set.
</ResponseField>

<RequestExample>
  ```py Simple theme={"system"}
  redis.zadd("key1", {"a": 1, "b": 2, "c": 3})

  redis.zadd("key2", {"c": 3, "d": 4, "e": 5})

  result = redis.zinterstore("dest", ["key1", "key2"])

  assert result == 1
  ```

  ```py Aggregation theme={"system"}
  redis.zadd("key1", {"a": 1, "b": 2, "c": 3})

  redis.zadd("key2", {"a": 3, "b": 4, "c": 5})

  result = redis.zinterstore("dest", ["key1", "key2"], withscores=True, aggregate="SUM")

  assert result == 3
  ```

  ```py Weights theme={"system"}
  redis.zadd("key1", {"a": 1})

  redis.zadd("key2", {"a": 1})

  result = redis.zinterstore("dest", ["key1", "key2"],
                        withscores=True,
                        aggregate="SUM",
                        weights=[2, 3])

  assert result == 1
  ```
</RequestExample>
