> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Error read ECONNRESET

### Symptom

The client can not connect to the database throwing an exception similar to:

```
[ioredis] Unhandled error event: Error: read ECONNRESET
    at TCP.onStreamRead (node:internal/stream_base_commons:211:20)
```

### Diagnosis

The server is TLS enabled but your connection (client) is not.

### Solution

Check your connection parameters and ensure you enable TLS.

If you are using a Redis URL then it should start with `rediss://`.

You can copy the correct client configuration from Upstash console clicking on
**Redis Connect** button.
