> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# LMOVE

> Move an element from one list to another.

## Arguments

<ParamField body="source" type="str" required>
  The key of the source list.
</ParamField>

<ParamField body="destination" type="str" required>
  The key of the destination list.
</ParamField>

<ParamField body="wherefrom" type="&#x22;left&#x22; | &#x22;right&#x22;" required>
  The side of the source list from which the element was popped.
</ParamField>

<ParamField body="whereto" type="&#x22;left&#x22; | &#x22;right&#x22;" required>
  The side of the destination list to which the element was pushed.
</ParamField>

## Response

<ResponseField type="str" required>
  The element that was moved.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.rpush("source", "one", "two", "three")
  redis.lpush("destination", "four", "five", "six")

  assert redis.lmove("source", "destination", "RIGHT", "LEFT") == "three"

  assert redis.lrange("source", 0, -1) == ["one", "two"]
  ```
</RequestExample>
