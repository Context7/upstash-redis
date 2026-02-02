> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Get Started with AWS Lambda

You can connect to Upstash database from your Lambda functions using your
favorite Redis client. You do not need any extra configuration. The only thing
to note is you should use the same region for your Lambda function and database
to minimize latency.

If you do not have any experience with AWS Lambda functions, you can follow the
following tutorial. The tutorial explains the required steps to implement an AWS
Lambda function that takes the key/value as parameters from APIGateway then
inserts an entry (key/value) to the database which is on Upstash. We have
implemented the function in Node.js, but the steps and the logic are quite
similar in other languages.

<Note>
  This example uses Redis clients. If you expect many concurrent AWS Lambda
  invocation then we recommend using
  **[upstash-redis](/redis/howto/connectwithupstashredis)** which is HTTP/REST
  based.
</Note>

**Step 1: Create database on Upstash**

If you do not have one, create a database following this
[guide](../overall/getstarted).

**Step 2: Create a Node project**

Create an empty folder for your project and inside the folder create a node
project with the command:

```
npm init
```

Then install the redis client with:

```
npm install ioredis
```

Now create index.js file. Replace the Redis URL in the below code.

<Snippet file="redis/ioredisnote.mdx" />

```javascript  theme={"system"}
var Redis = require("ioredis");

if (typeof client === "undefined") {
  var client = new Redis("rediss://:YOUR_PASSWORD@YOUR_ENDPOINT:YOUR_PORT");
}
exports.handler = async (event) => {
  await client.set("foo", "bar");
  let result = await client.get("foo");
  let response = {
    statusCode: 200,
    body: JSON.stringify({
      result: result,
    }),
  };
  return response;
};
```

**Step 3: Deploy Your Function**

Our function is ready to deploy. Normally you could copy-paste your function
code to AWS Lambda editor. But here it is not possible because we have an extra
dependency (redis-client). So we will zip and upload our function.

When you are in your project folder, create a zip with this command:

```
zip -r app.zip .
```

Now open your AWS console, from the top-right menu, select the region that you
created your database in Upstash. Then find or search the lambda service, click
on `Create Function` button.

<Frame>
  <img src="https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/awslambda/createfunction.png?fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=41a2318c6d70be9672dc2723a98fb594" width="100%" data-og-width="2610" data-og-height="1460" data-path="img/awslambda/createfunction.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/awslambda/createfunction.png?w=280&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=a2b35239fbd7e114999b7db335f964cf 280w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/awslambda/createfunction.png?w=560&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=b3db2b6794c47d93a5eddcdd233e1005 560w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/awslambda/createfunction.png?w=840&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=a7d4afb3039459c4adc9961135b697e0 840w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/awslambda/createfunction.png?w=1100&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=2cf57b76ccaecae1e6c9f8b644738a02 1100w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/awslambda/createfunction.png?w=1650&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=bfeab75ee6b738536bff6baf139206ad 1650w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/awslambda/createfunction.png?w=2500&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=92790c5c7670d5f8180a4c180de339af 2500w" />
</Frame>

Enter a name for your function and select `Node.js 14.x` as runtime. Click
`Create Function`.

Now you are on the function screen, scroll below to `Function Code` section. On
`Code entry type` selection, select `Upload a .zip file`. Upload the `app.zip`
file you have just created and click on the `Save` button on the top-right. You
need to see your code as below:

<Frame>
  <img src="https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/awslambda/functioncode.png?fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=592b191224ba6ee04d13f67cdf130f3e" width="100%" data-og-width="2556" data-og-height="1250" data-path="img/awslambda/functioncode.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/awslambda/functioncode.png?w=280&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=38b094a1768c9545f3fc42e2646a83c0 280w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/awslambda/functioncode.png?w=560&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=3ac03f629bc106b193abea0d6845bb95 560w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/awslambda/functioncode.png?w=840&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=b68484c37611965f654ac08b9b63ca10 840w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/awslambda/functioncode.png?w=1100&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=e414f38dd6363f42cada7235a41ec733 1100w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/awslambda/functioncode.png?w=1650&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=44e457af19727ac7aacef929ef914571 1650w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/awslambda/functioncode.png?w=2500&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=1ae2f984255e4ce6c11f862783311e8d 2500w" />
</Frame>

Now you can test your code. Click on the `Test` button on the top right. Create
an event like the below:

```
{
  "key": "foo",
  "value": "bar"
}
```

Now, click on Test. You will see something like this:

<Frame>
  <img src="https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/awslambda/success.png?fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=d7b295ca30abb4c9925ea3c6de34176c" width="100%" data-og-width="1884" data-og-height="832" data-path="img/awslambda/success.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/awslambda/success.png?w=280&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=79680feab46a3a3d391388b5e8e14a3b 280w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/awslambda/success.png?w=560&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=c39790f9d2853d3d50e2af791927f6bc 560w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/awslambda/success.png?w=840&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=59a3ac6431fedf667ecc3984f2dc7b33 840w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/awslambda/success.png?w=1100&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=d24ddbd3a73dce1e513039eb1934161d 1100w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/awslambda/success.png?w=1650&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=0f33665fc23e464f5440e1f77567e5a3 1650w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/awslambda/success.png?w=2500&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=7261209a27b3c2497bf216fceb1c4cee 2500w" />
</Frame>

Congratulations, now your lambda function inserts entry to your Upstash
database.

**What can be the next?**

* You can write and deploy another function to just get values from the
  database.
* You can learn better ways to deploy your functions such as
  [serverless framework](https://serverless.com/) and
  [AWS SAM](https://aws.amazon.com/serverless/sam/)
* You can integrate
  [API Gateway](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-create-api-as-simple-proxy-for-lambda.html)
  so you can call your function via http.
* You can learn about how to monitor your functions from CloudWatch as described
  [here](https://docs.aws.amazon.com/lambda/latest/dg//monitoring-functions-logs.html)
  .

#### Redis Connections in AWS Lambda

Although Redis connections are very lightweight, a new connection inside each
Lambda function can cause a notable latency. On the other hand, reusing Redis
connections inside the AWS Lambda functions has its own drawbacks. When AWS
scales out Lambda functions, the number of open connections can rapidly
increase. Fortunately, Upstash detects and terminates the idle and zombie
connections thanks to its smart connection handling algorithm. Since this
algorithm is used; we have been recommending caching your Redis connection in
serverless functions.

<Info>
  See [the blog post](https://blog.upstash.com/serverless-database-connections)
  about the database connections in serverless functions.
</Info>

Below is our findings about various Redis clients' behaviours when connection is
created, a single command is submitted and then connection is closed. **Note
that these commands (AUTH, INFO, PING, QUIT, COMMAND) are not billed.**

| Client                                                | #Commands |   Issued Commands  |
| ----------------------------------------------------- | :-------: | :----------------: |
| [redis-cli](https://redis.io/topics/rediscli)         |     2     |   AUTH - COMMAND   |
| [node-redis](https://github.com/NodeRedis/node-redis) |     3     | AUTH - INFO - QUIT |
| [ioredis](https://github.com/luin/ioredis)            |     3     | AUTH - INFO - QUIT |
| [redis-py](https://github.com/andymccurdy/redis-py)   |     1     |        AUTH        |
| [jedis](https://github.com/xetorthio/jedis)           |     2     |     AUTH - QUIT    |
| [lettuce](https://github.com/lettuce-io/lettuce-core) |     2     |     AUTH - QUIT    |
| [go-redis](https://github.com/go-redis/redis)         |     1     |        AUTH        |
