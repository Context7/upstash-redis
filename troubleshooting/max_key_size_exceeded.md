> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# ERR max key size exceeded

### Symptom

The client gets an exception similar to:

```
ReplyError: ERR max key size exceeded. Limit: X bytes, Actual: Z bytes
```

### Diagnosis

Size of the key in the request exceeds the max key size limit, which is `32Kb`.

### Solution

This is a hardcoded limit and cannot be configured per database. You should
reduce the key size.
