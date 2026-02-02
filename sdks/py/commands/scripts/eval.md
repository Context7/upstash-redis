> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# EVAL

> Evaluate a Lua script server side.

## Arguments

<ParamField body="script" type="str" required>
  The lua script to run.
</ParamField>

<ParamField body="keys" type="List[str]" required>
  All of the keys accessed in the script
</ParamField>

<ParamField body="args" type="unknown[]" required>
  All of the arguments you passed to the script
</ParamField>

## Response

<ResponseField type="Any" required>
  The result of the script.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  script = """
  local value = redis.call("GET", KEYS[1])
  return value
  """

  redis.set("mykey", "Hello")

  assert redis.eval(script, keys=["mykey"]) == "Hello"
  ```

  ```py Accepting arguments theme={"system"}
  assert redis.eval("return ARGV[1]", args=["Hello"]) == "Hello"
  ```
</RequestExample>
