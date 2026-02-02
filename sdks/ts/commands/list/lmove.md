> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# LMOVE

> Move an element from one list to another.

## Arguments

<ParamField body="source" type="string" required>
  The key of the source list.
</ParamField>

<ParamField body="destination" type="string" required>
  The key of the destination list.
</ParamField>

<ParamField body="from" type="&#x22;left&#x22; | &#x22;right&#x22;" required>
  The side of the source list from which the element was popped.
</ParamField>

<ParamField body="to" type="&#x22;left&#x22; | &#x22;right&#x22;" required>
  The side of the destination list to which the element was pushed.
</ParamField>

## Response

<ResponseField type="TValue" required>
  The element that was moved.
</ResponseField>

<RequestExample>
  ```ts Example theme={"system"}
   await redis.rpush("source", "a", "b", "c"); 
   const element = await redis.move("source", "destination", "left", "left");  
  ```
</RequestExample>
