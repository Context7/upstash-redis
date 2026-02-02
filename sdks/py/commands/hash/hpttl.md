> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# HPTTL

> Retrieves the remaining time-to-live (TTL) for field(s) in a hash in milliseconds.

## Arguments

<ParamField body="key" type="str" required>
  The key of the hash.
</ParamField>

<ParamField body="fields" type="Union[str, List[str]]" required>
  The field or list of fields to retrieve the TTL for.
</ParamField>

## Response

<ResponseField type="List[int]" required>
  A list of integers representing the remaining TTL in milliseconds for each field.

  * `-2` if the field does not exist in the hash or if the key doesn't exist.
  * `-1` if the field exists but has no associated expiration.

  For more details, see [HPTTL documentation](https://redis.io/commands/hpttl).
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  redis.hset(hash_name, field, value)
  redis.hpexpire(hash_name, field, 1000)

  assert redis.hpttl(hash_name, field) == [950]
  ```
</RequestExample>
