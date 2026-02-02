> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# JSON.MSET

> Sets multiple JSON values at multiple paths in multiple keys.

## Arguments

<ParamField body="params" type="{ key: string, path: string, value: TData }[]" required>
  A list of objects where each tuple contains a key, a path, and a value.
  Type of value (`TData`) can be `Array<number>`, `string`, `boolean`, `Record<string, any>`, or `Array<any>`.
</ParamField>

## Response

<ResponseField type="string" required>
  Returns "OK" if the command was successful.
</ResponseField>

<RequestExample>
  ```py Example theme={"system"}
  await redis.json.mset([
    { key: key, path: "$.path", value: value}, 
    { key: key2, path: "$.path2", value: value2}
  ])
  ```
</RequestExample>
