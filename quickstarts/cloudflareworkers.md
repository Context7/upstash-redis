> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

#  Cloudflare Workers

### Database Setup

Create a Redis database using [Upstash Console](https://console.upstash.com) or
[Upstash CLI](https://github.com/upstash/cli).

### Project Setup

We will use **C3 (create-cloudflare-cli)** command-line tool to create our application. You can open a new terminal window and run C3 using the prompt below.

<CodeGroup>
  ```shell npm theme={"system"}
  npm create cloudflare@latest -- upstash-redis-worker
  ```

  ```shell yarn theme={"system"}
  yarn create cloudflare upstash-redis-worker
  ```

  ```shell pnpm theme={"system"}
  pnpm create cloudflare upstash-redis-worker
  ```
</CodeGroup>

This will create a new Cloudflare Workers project:

```text  theme={"system"}
➜  npm create cloudflare@latest -- upstash-redis-worker

> npx
> create-cloudflare upstash-redis-worker


─────────────────────────────────────────────────────────────────────────────────────────────────
👋 Welcome to create-cloudflare v2.50.8!
🧡 Let's get started.
📊 Cloudflare collects telemetry about your usage of Create-Cloudflare.

Learn more at: https://github.com/cloudflare/workers-sdk/blob/main/packages/create-cloudflare/telemetry.md
─────────────────────────────────────────────────────────────────────────────────────────────────

╭ Create an application with Cloudflare Step 1 of 3
│
├ In which directory do you want to create your application?
│ dir ./upstash-redis-worker
│
├ What would you like to start with?
│ category Hello World example
│
├ Which template would you like to use?
│ type Worker only
│
├ Which language do you want to use?
│ lang TypeScript
│
├ Copying template files
│ files copied to project directory
│
├ Updating name in `package.json`
│ updated `package.json`
│
├ Installing dependencies
│ installed via `npm install`
│
╰ Application created 

...

────────────────────────────────────────────────────────────
🎉  SUCCESS  Application created successfully!
```

We will also install the **Upstash Redis SDK** to connect to Redis.

```bash  theme={"system"}
npm install @upstash/redis
```

### The Code

Here is a Worker template to configure and test Upstash Redis connection.

<CodeGroup>
  ```ts src/index.ts theme={"system"}
  import { Redis } from "@upstash/redis/cloudflare";

  export interface Env {
    UPSTASH_REDIS_REST_URL: string;
    UPSTASH_REDIS_REST_TOKEN: string;
  }

  export default {
  	async fetch(request, env, ctx): Promise<Response> {
  		const redis = Redis.fromEnv(env);
  		const count = await redis.incr("counter");
  		return new Response(JSON.stringify({ count }));
  		
  	},
  } satisfies ExportedHandler<Env>;

  ```

  ```js src/index.js theme={"system"}
  import { Redis } from "@upstash/redis/cloudflare";

  export default {
    async fetch(request, env, ctx) {
      const redis = Redis.fromEnv(env);
      const count = await redis.incr("counter");
      return new Response(JSON.stringify({ count }));
    },
  };
  ```
</CodeGroup>

### Configure Credentials

There are two methods for setting up the credentials for Redis. One for worker level, the other for account level.

#### Using Cloudflare Secrets (Worker Level Secrets)

This is the common way of creating secrets for your worker, see [Workflow Secrets](https://developers.cloudflare.com/workers/configuration/secrets/)

* Navigate to [Upstash Console](https://console.upstash.com) and get your Redis credentials.

* In [Cloudflare Dashboard](https://dash.cloudflare.com/), Go to **Compute (Workers)** > **Workers & Pages**.

* Select your worker and go to **Settings** > **Variables and Secrets**.

* Add your Redis credentials as secrets here:

<Frame>
  <img src="https://mintcdn.com/upstash/DrxIz7v3jaqUZCku/img/cloudflare-integration/redis-secrets.png?fit=max&auto=format&n=DrxIz7v3jaqUZCku&q=85&s=890eabf39148b839095a2c12a516345b" data-og-width="1716" width="1716" data-og-height="626" height="626" data-path="img/cloudflare-integration/redis-secrets.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/DrxIz7v3jaqUZCku/img/cloudflare-integration/redis-secrets.png?w=280&fit=max&auto=format&n=DrxIz7v3jaqUZCku&q=85&s=1a7745e9dbb4f40efb1800ccc93e285c 280w, https://mintcdn.com/upstash/DrxIz7v3jaqUZCku/img/cloudflare-integration/redis-secrets.png?w=560&fit=max&auto=format&n=DrxIz7v3jaqUZCku&q=85&s=cfdfa08edd78b912a51b0d453b066076 560w, https://mintcdn.com/upstash/DrxIz7v3jaqUZCku/img/cloudflare-integration/redis-secrets.png?w=840&fit=max&auto=format&n=DrxIz7v3jaqUZCku&q=85&s=afb7d787d4aafae317fd1e541d61d942 840w, https://mintcdn.com/upstash/DrxIz7v3jaqUZCku/img/cloudflare-integration/redis-secrets.png?w=1100&fit=max&auto=format&n=DrxIz7v3jaqUZCku&q=85&s=bb69c86b2e587273b6d679fa7758b93f 1100w, https://mintcdn.com/upstash/DrxIz7v3jaqUZCku/img/cloudflare-integration/redis-secrets.png?w=1650&fit=max&auto=format&n=DrxIz7v3jaqUZCku&q=85&s=c9d225dce59a3386eae154a2e9eae85b 1650w, https://mintcdn.com/upstash/DrxIz7v3jaqUZCku/img/cloudflare-integration/redis-secrets.png?w=2500&fit=max&auto=format&n=DrxIz7v3jaqUZCku&q=85&s=c694a40ad032e0b41315bfd9b95b82cb 2500w" />
</Frame>

#### Using Cloudflare Secrets Store (Account Level Secrets)

This method requires a few modifications in the worker code, see [Access to Secret on Env Object](https://developers.cloudflare.com/secrets-store/integrations/workers/#3-access-the-secret-on-the-env-object)

```ts src/index.ts theme={"system"}
import { Redis } from "@upstash/redis/cloudflare";

export interface Env {
  UPSTASH_REDIS_REST_URL: SecretsStoreSecret;
  UPSTASH_REDIS_REST_TOKEN: SecretsStoreSecret;
}

export default {
	async fetch(request, env, ctx): Promise<Response> {
		const redis = Redis.fromEnv({
			UPSTASH_REDIS_REST_URL: await env.UPSTASH_REDIS_REST_URL.get(),
			UPSTASH_REDIS_REST_TOKEN: await env.UPSTASH_REDIS_REST_TOKEN.get(),
		});
		const count = await redis.incr("counter");
		return new Response(JSON.stringify({ count }));

	},
} satisfies ExportedHandler<Env>;
```

After doing these modifications, you can deploy the worker to Cloudflare with `npx wrangler deploy`, and
follow the steps below to define the secrets:

* Navigate to [Upstash Console](https://console.upstash.com) and get your Redis credentials.

* In [Cloudflare Dashboard](https://dash.cloudflare.com/), Go to **Secrets Store** and add Redis credentials as secrets.

<Frame>
  <img src="https://mintcdn.com/upstash/DrxIz7v3jaqUZCku/img/cloudflare-integration/redis-secrets-store.png?fit=max&auto=format&n=DrxIz7v3jaqUZCku&q=85&s=f8cd7072110966eaf77fff1b6a7d8254" data-og-width="1940" width="1940" data-og-height="1110" height="1110" data-path="img/cloudflare-integration/redis-secrets-store.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/DrxIz7v3jaqUZCku/img/cloudflare-integration/redis-secrets-store.png?w=280&fit=max&auto=format&n=DrxIz7v3jaqUZCku&q=85&s=0ed4848f21aad699b9a4deddfdc196dc 280w, https://mintcdn.com/upstash/DrxIz7v3jaqUZCku/img/cloudflare-integration/redis-secrets-store.png?w=560&fit=max&auto=format&n=DrxIz7v3jaqUZCku&q=85&s=48d16bca52c3f4212a6119906c795384 560w, https://mintcdn.com/upstash/DrxIz7v3jaqUZCku/img/cloudflare-integration/redis-secrets-store.png?w=840&fit=max&auto=format&n=DrxIz7v3jaqUZCku&q=85&s=dfa548e4102eb279f5dde6533d12bd3c 840w, https://mintcdn.com/upstash/DrxIz7v3jaqUZCku/img/cloudflare-integration/redis-secrets-store.png?w=1100&fit=max&auto=format&n=DrxIz7v3jaqUZCku&q=85&s=01725e656a74c38d5457f9af1c75dd49 1100w, https://mintcdn.com/upstash/DrxIz7v3jaqUZCku/img/cloudflare-integration/redis-secrets-store.png?w=1650&fit=max&auto=format&n=DrxIz7v3jaqUZCku&q=85&s=672afadaa6fc60efdc0bec66f7a4a7ed 1650w, https://mintcdn.com/upstash/DrxIz7v3jaqUZCku/img/cloudflare-integration/redis-secrets-store.png?w=2500&fit=max&auto=format&n=DrxIz7v3jaqUZCku&q=85&s=4760d6eff8516994b0bc185d3f833335 2500w" />
</Frame>

* Under **Compute (Workers)** > **Workers & Pages**, find your worker and add these secrets as bindings.

<Frame>
  <img src="https://mintcdn.com/upstash/DrxIz7v3jaqUZCku/img/cloudflare-integration/redis-add-binding.png?fit=max&auto=format&n=DrxIz7v3jaqUZCku&q=85&s=840e39008f8888642accf0dc1c44a641" data-og-width="1940" width="1940" data-og-height="1370" height="1370" data-path="img/cloudflare-integration/redis-add-binding.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/DrxIz7v3jaqUZCku/img/cloudflare-integration/redis-add-binding.png?w=280&fit=max&auto=format&n=DrxIz7v3jaqUZCku&q=85&s=b0991567a3c4eb6075f26a148b9c9c60 280w, https://mintcdn.com/upstash/DrxIz7v3jaqUZCku/img/cloudflare-integration/redis-add-binding.png?w=560&fit=max&auto=format&n=DrxIz7v3jaqUZCku&q=85&s=337e5484907c1199cc92407c86b4e4b0 560w, https://mintcdn.com/upstash/DrxIz7v3jaqUZCku/img/cloudflare-integration/redis-add-binding.png?w=840&fit=max&auto=format&n=DrxIz7v3jaqUZCku&q=85&s=c66555178015dfa8e395893352458048 840w, https://mintcdn.com/upstash/DrxIz7v3jaqUZCku/img/cloudflare-integration/redis-add-binding.png?w=1100&fit=max&auto=format&n=DrxIz7v3jaqUZCku&q=85&s=55f59d8885adfdbd187db6f4503d1cd0 1100w, https://mintcdn.com/upstash/DrxIz7v3jaqUZCku/img/cloudflare-integration/redis-add-binding.png?w=1650&fit=max&auto=format&n=DrxIz7v3jaqUZCku&q=85&s=688c3420d6b6644e9147c8555a9008b1 1650w, https://mintcdn.com/upstash/DrxIz7v3jaqUZCku/img/cloudflare-integration/redis-add-binding.png?w=2500&fit=max&auto=format&n=DrxIz7v3jaqUZCku&q=85&s=6503005e5fec4dbbaa13246fee4533b9 2500w" />
</Frame>

### Deployment

<Note>
  Newer deployments may revert the configurations you did in the dashboard.
  While worker level secrets persist, the bindings will be gone!
</Note>

Deploy your function to Cloudflare with `npx wrangler deploy`

The endpoint of the function will be provided to you, once the deployment is done.

### Testing

Open a different terminal and test the endpoint. Note the destination
url is the same that was printed in the previous deploy step.

```bash  theme={"system"}
curl -X POST 'https://<your-worker-name>.<account-name>.workers.dev' \
     -H 'Content-Type: application/json' 
```

The response will be in the format of `{"count":20}`

In the logs you should see something like this:

```bash  theme={"system"}
$ npx wrangler tail

⛅️ wrangler 4.43.0
--------------------

Successfully created tail, expires at 2025-10-16T18:59:18Z
Connected to <your-worker-name>, waiting for logs...
POST https://<your-worker-name>.<account-name>.workers.dev/ - Ok @ 10/16/2025, 4:05:30 PM
```

## Repositories

Javascript:
[https://github.com/upstash/upstash-redis/tree/main/examples/cloudflare-workers](https://github.com/upstash/upstash-redis/tree/main/examples/cloudflare-workers)

Typescript:
[https://github.com/upstash/upstash-redis/tree/main/examples/cloudflare-workers-with-typescript](https://github.com/upstash/upstash-redis/tree/main/examples/cloudflare-workers-with-typescript)
