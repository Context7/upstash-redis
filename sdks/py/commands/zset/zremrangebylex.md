> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# ZREMRANGEBYLEX

> Remove all members in a sorted set between the given lexicographical range.

## Arguments

<ParamField body="key" type="str" required>
  The key of the sorted set
</ParamField>

<ParamField body="min" type="str" required>
  The minimum lexicographical value to remove.
</ParamField>

<ParamField body="min" type="str" required>
  The maximum lexicographical value to remove.
</ParamField>

## Response

<ResponseField type="int" required>
  The number of elements removed from the sorted set.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.zremrangebylex("key", "alpha", "omega")
  ```
</RequestExample>
