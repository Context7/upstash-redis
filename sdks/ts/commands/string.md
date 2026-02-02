> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# String Commands

## MGET

Load multiple keys at once. For billing purposes, this counts as a single command.

If a key is not found, it will be returned as `null`, so you might end up with `null` values in your response array.

```ts  theme={"system"}
const values = await redis.mget("key1", "key2", "key3");
```

## MSET

Set multiple values at once. For billing purposes, this counts as a single command.

```ts  theme={"system"}
await redis.mset({
  key1: { a: 1 },
  key2: "value2",
  key3: true,
});
```

## MSETNX

```ts  theme={"system"}
```

## PSETEX

```ts  theme={"system"}
```

## SET

```ts  theme={"system"}
```

## SETEX

```ts  theme={"system"}
```

## SETNX

```ts  theme={"system"}
```

## SETRANGE

```ts  theme={"system"}
```

## STRLEN

```ts  theme={"system"}
```

## SUBSTR

```ts  theme={"system"}
```
