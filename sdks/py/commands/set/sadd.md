> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# SADD

> Adds one or more members to a set.

## Arguments

<ParamField body="key" type="str" required>
  The key of the set.
</ParamField>

<ParamField body="members" type="...TValue[]" required>
  One or more members to add to the set.
</ParamField>

## Response

<ResponseField type="number" required>
  The number of elements that were added to the set, not including all the elements already present in the set.
</ResponseField>

<RequestExample>
  ```py Example  theme={"system"}
  assert redis.sadd("key", "a", "b", "c") == 3
  ```
</RequestExample>
