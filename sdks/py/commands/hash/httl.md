> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# HTTL

> Retrieves the remaining time-to-live (TTL) for field(s) in a hash in seconds.

## Arguments

<ParamField body="key" type="str" required>
  The key of the hash.
</ParamField>

<ParamField body="fields" type="Union[str, List[str]]" required>
  The field or list of fields to retrieve the TTL for.
</ParamField>

## Response

<ResponseField type="List[int]" required>
  A list of integers representing the remaining TTL in seconds for each field.

  * `-2` if the field does not exist in the hash or if the key doesn't exist.
  * `-1` if the field exists but has no associated expiration.

  For more details, see [HTTL documentation](https://redis.io/commands/httl).
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.hset(hash_name, field, value)
  redis.hexpire(hash_name, field, 10)

  assert redis.httl(hash_name, field) == [9]
  ```
</RequestExample>
