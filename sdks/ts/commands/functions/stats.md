> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# FUNCTION STATS

> Return information about the function running engine.

## Response

<ResponseField type="Object" required>
  Stats about the engines and functions.

  <Note>
    Currently, `LUA` is the only supported engine.
  </Note>

  <Expandable>
    <ParamField body="engines" type="Object">
      <Expandable>
        <ParamField body="LUA" type="Object">
          <Expandable>
            <ParamField body="librariesCount" type="number">
              The number of libraries.
            </ParamField>

            <ParamField body="functionsCount" type="number">
              The number of functions.
            </ParamField>
          </Expandable>
        </ParamField>
      </Expandable>
    </ParamField>
  </Expandable>
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
  const stats = await redis.functions.stats()

  console.log(stats)
  // {
  //   engines: {
  //     LUA: {
  //       librariesCount: 3,
  //       functionsCount: 15
  //     }
  //   }
  // }
  ```
</RequestExample>
