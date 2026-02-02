> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# SST v2

<Card title="GitHub Repository" icon="github" href="https://github.com/upstash/redis-js/tree/main/examples/sst-v2" horizontal>
  You can find the project source code on GitHub.
</Card>

### Prerequisites

You need to have AWS credentials configured locally.

1. [Create an AWS account](https://aws.amazon.com/)
2. [Create an IAM user](https://sst.dev/chapters/create-an-iam-user.html)
3. [Configure the AWS CLI](https://sst.dev/chapters/configure-the-aws-cli.html)

### Project Setup

Let's create a new SST + Next.js application.

```shell  theme={"system"}
npx create-sst@latest --template standard/nextjs
cd my-sst-app
npm install
```

Install the `@upstash/redis` package.

```shell  theme={"system"}
npm install @upstash/redis
```

### Database Setup

Create a Redis database using [Upstash Console](https://console.upstash.com) or [Upstash CLI](https://github.com/upstash/cli) and copy the `UPSTASH_REDIS_REST_URL` and `UPSTASH_REDIS_REST_TOKEN` into your `.env` file.

```shell  theme={"system"}
npx sst secrets set UPSTASH_REDIS_REST_URL <YOUR_URL>
npx sst secrets set UPSTASH_REDIS_REST_TOKEN <YOUR_TOKEN>
```

### Bind the Secrets

```ts /stacks/Default.ts theme={"system"}
import { Config, StackContext, NextjsSite } from "sst/constructs";

export function Default({ stack }: StackContext) {
  const UPSTASH_REDIS_REST_URL = new Config.Secret(stack, "UPSTASH_REDIS_REST_URL");
  const UPSTASH_REDIS_REST_TOKEN = new Config.Secret(stack, "UPSTASH_REDIS_REST_TOKEN");
  const site = new NextjsSite(stack, "site", {
    bind: [UPSTASH_REDIS_REST_URL, UPSTASH_REDIS_REST_TOKEN],
    path: "packages/web",
  });
  stack.addOutputs({
    SiteUrl: site.url,
  });
}
```

### API Setup

```ts /packages/web/pages/api/hello.ts theme={"system"}
import { Redis } from "@upstash/redis";
import type { NextApiRequest, NextApiResponse } from "next";
import { Config } from "sst/node/config";

const redis = new Redis({
  url: Config.UPSTASH_REDIS_REST_URL,
  token: Config.UPSTASH_REDIS_REST_TOKEN,
  });

export default async function handler(
  req: NextApiRequest,
  res: NextApiResponse,
) {
  const count = await redis.incr("counter");
  res.status(200).json({ count });
}

```

### Run

Run the SST app.

```shell  theme={"system"}
npm run dev
```

After prompted, run the Next.js app.

```shell  theme={"system"}
cd packages/web
npm run dev
```

Check `http://localhost:3000/api/hello`

### Deploy

Set the secrets for the prod stage.

```shell  theme={"system"}
npx sst secrets set --stage prod UPSTASH_REDIS_REST_URL <YOUR_URL>
npx sst secrets set --stage prod UPSTASH_REDIS_REST_TOKEN <YOUR_TOKEN>
```

Deploy with SST.

```shell  theme={"system"}
npx sst deploy --stage prod
```

Check `<SiteUrl>/api/hello` with the given SiteUrl.
