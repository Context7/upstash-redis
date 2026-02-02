> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# WRONGPASS invalid or missing auth token

### Symptom

The database rejects your request with an error similar to:

```
UpstashError: WRONGPASS invalid or missing auth token
```

### Diagnosis

The server rejects your request because the auth token is missing or invalid.

Most likely you have forgotten to set it in your environment variables, or you
are using a wrong token.

The connection password can only be used in traditional Redis clients. If you
want to connect over HTTP, you need to use the HTTP auth token.

### Solution

1. Check that you have set the `UPSTASH_REDIS_REST_TOKEN` in your environment
   variables and it is loaded correctly by your application at runtime.

2. Make sure you are using the correct HTTP auth token. You can copy the correct
   client configuration from the
   [Upstash console](https://console.upstash.com/redis) by copying the snippet
   from the `Connect to your database` -> `@upstash/redis` tab

<img src="https://mintcdn.com/upstash/EFJsv57gEAWfBXNv/img/troubleshooting/rest/console_upstash_redis.png?fit=max&auto=format&n=EFJsv57gEAWfBXNv&q=85&s=6209760b747138fc787943506a201252" alt="" data-og-width="1981" width="1981" data-og-height="730" height="730" data-path="img/troubleshooting/rest/console_upstash_redis.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/EFJsv57gEAWfBXNv/img/troubleshooting/rest/console_upstash_redis.png?w=280&fit=max&auto=format&n=EFJsv57gEAWfBXNv&q=85&s=4ae457f93cdb787f8fb1b7bb51aa607a 280w, https://mintcdn.com/upstash/EFJsv57gEAWfBXNv/img/troubleshooting/rest/console_upstash_redis.png?w=560&fit=max&auto=format&n=EFJsv57gEAWfBXNv&q=85&s=b2fefb3e70f7b9e106fcdfa90c2c3b4e 560w, https://mintcdn.com/upstash/EFJsv57gEAWfBXNv/img/troubleshooting/rest/console_upstash_redis.png?w=840&fit=max&auto=format&n=EFJsv57gEAWfBXNv&q=85&s=90a2ffdc9ca1652050aff49efd3f1dab 840w, https://mintcdn.com/upstash/EFJsv57gEAWfBXNv/img/troubleshooting/rest/console_upstash_redis.png?w=1100&fit=max&auto=format&n=EFJsv57gEAWfBXNv&q=85&s=d72ff8142eb9b2703caf02855dbd5d84 1100w, https://mintcdn.com/upstash/EFJsv57gEAWfBXNv/img/troubleshooting/rest/console_upstash_redis.png?w=1650&fit=max&auto=format&n=EFJsv57gEAWfBXNv&q=85&s=e5136fc555176898fda2633ce154d1bb 1650w, https://mintcdn.com/upstash/EFJsv57gEAWfBXNv/img/troubleshooting/rest/console_upstash_redis.png?w=2500&fit=max&auto=format&n=EFJsv57gEAWfBXNv&q=85&s=12ec155de0a225f79f855145ab8b0018 2500w" />

Or scroll further down to the `REST API` section and copy the
`UPSTASH_REDIS_REST_URL` and `UPSTASH_REDIS_REST_TOKEN` from there.

<img src="https://mintcdn.com/upstash/EFJsv57gEAWfBXNv/img/troubleshooting/rest/console_rest_api.png?fit=max&auto=format&n=EFJsv57gEAWfBXNv&q=85&s=0f64cdc01036d9144a9f35d544f6baf3" alt="" data-og-width="1981" width="1981" data-og-height="764" height="764" data-path="img/troubleshooting/rest/console_rest_api.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/EFJsv57gEAWfBXNv/img/troubleshooting/rest/console_rest_api.png?w=280&fit=max&auto=format&n=EFJsv57gEAWfBXNv&q=85&s=9500d27d655732d9c170ec9a9d5b4192 280w, https://mintcdn.com/upstash/EFJsv57gEAWfBXNv/img/troubleshooting/rest/console_rest_api.png?w=560&fit=max&auto=format&n=EFJsv57gEAWfBXNv&q=85&s=feb6821d6de3810083e7f7121a3b2fab 560w, https://mintcdn.com/upstash/EFJsv57gEAWfBXNv/img/troubleshooting/rest/console_rest_api.png?w=840&fit=max&auto=format&n=EFJsv57gEAWfBXNv&q=85&s=cd2e074c8767f9d1ba413d2cfc796132 840w, https://mintcdn.com/upstash/EFJsv57gEAWfBXNv/img/troubleshooting/rest/console_rest_api.png?w=1100&fit=max&auto=format&n=EFJsv57gEAWfBXNv&q=85&s=5c73b679a9202d0eb90f042b8f216579 1100w, https://mintcdn.com/upstash/EFJsv57gEAWfBXNv/img/troubleshooting/rest/console_rest_api.png?w=1650&fit=max&auto=format&n=EFJsv57gEAWfBXNv&q=85&s=2e8848bb2ae95f1bdca73490439aa4aa 1650w, https://mintcdn.com/upstash/EFJsv57gEAWfBXNv/img/troubleshooting/rest/console_rest_api.png?w=2500&fit=max&auto=format&n=EFJsv57gEAWfBXNv&q=85&s=7dd7cffe9ce3651a0a4a4e95e45399bd 2500w" />
