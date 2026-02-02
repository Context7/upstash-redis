> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# EXPIRE

> Sets a timeout on key. The key will automatically be deleted.

## Arguments

<ParamField body="key" type="str" required>
  The key to set the timeout on.
</ParamField>

<ParamField body="seconds" type="int | datetime.timedelta" required>
  The timeout in seconds as int or datetime.timedelta object
</ParamField>

<ParamField body="nx" type="bool">
  Set expiry only when the key has no expiry
</ParamField>

<ParamField body="xx" type="bool">
  Set expiry only when the key has an existing expiry
</ParamField>

<ParamField body="gt" type="bool">
  Set expiry only when the new expiry is greater than current one
</ParamField>

<ParamField body="lt" type="bool">
  Set expiry only when the new expiry is less than current one
</ParamField>

## Response

<ResponseField type="bool">
  `True` if the timeout was set
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  # With seconds
  redis.set("mykey", "Hello")
  redis.expire("mykey", 5)

  assert redis.get("mykey") == "Hello"

  time.sleep(5)

  assert redis.get("mykey") is None

  # With a timedelta
  redis.set("mykey", "Hello")
  redis.expire("mykey", datetime.timedelta(seconds=5))
  ```
</RequestExample>
