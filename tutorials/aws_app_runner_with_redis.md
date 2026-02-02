> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Build Stateful Applications with AWS App Runner and Serverless Redis

> This tutorial shows how to create a serverless and stateful application using AWS App Runner and Redis

AWS App Runner is a container service where AWS runs and scales your container
in a serverless way. The container storage is ephemeral so you should keep the
state in an external data store. In this tutorial we will build a simple
application which will keep the state on Redis and deploy the application to AWS
App Runner.

### The Stack

* Serverless compute: AWS App Runner (Node.js)
* Serverless data store: Redis via Upstash
* Deployment source: github repo

### Project Setup

Create a directory for your project:

```
mkdir app_runner_example

cd app_runner_example
```

Create a node project and install dependencies:

```
npm init

npm install ioredis
```

Create a Redis DB from [Upstash](https://console.upstash.com). In the database
details page, copy the connection code (Node tab).

### The Code

In your node project folder, create server.js and copy the below code:

```javascript  theme={"system"}
var Redis = require("ioredis");
const http = require("http");

if (typeof client === "undefined") {
  var client = new Redis(process.env.REDIS_URL);
}

const requestListener = async function (req, res) {
  if (req.url !== "/favicon.ico") {
    let count = await client.incr("counter");
    res.writeHead(200);
    res.end("Page view:" + count);
  }
};

const server = http.createServer(requestListener);
server.listen(8080);
```

<Snippet file="redis/ioredisnote.mdx" />

As you see, the code simple increment a counter on Redis and returns the
response as the page view count.

### Deployment

You have two options to deploy your code to the App Runner. You can either share
your Github repo with AWS or register your docker image to ECR. In this
tutorial, we will share
[our Github repo](https://github.com/upstash/app_runner_example) with App
Runner.

Create a github repo for your project and push your code. In AWS console open
the App Runner service. Click on `Create Service` button. Select
`Source code repository` option and add your repository by connecting your
Github and AWS accounts.

<Frame>
  <img src="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/apprunner/source.png?fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=257c8e3c17c49e7ce4d540c115a44ab4" width="800" data-og-width="1690" data-og-height="1792" data-path="img/examples/apprunner/source.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/apprunner/source.png?w=280&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=9a0f79f37bf280d8d02ac5dbdedbfee8 280w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/apprunner/source.png?w=560&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=d68a216826709130447784bcd48c7d9e 560w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/apprunner/source.png?w=840&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=4367057cffb506ca6baf8a863342fe2d 840w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/apprunner/source.png?w=1100&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=5cdf9e0c158382c5cc9aa3a631dfb0f5 1100w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/apprunner/source.png?w=1650&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=2f54cf24a72fd76749cf73c887017215 1650w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/apprunner/source.png?w=2500&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=d70e31e959cedeccf917ed656c0e662c 2500w" />
</Frame>

In the next page, choose `Nodejs 12` as your runtime, `npm install` as your
build command, `node server` as your start command and `8080` as your port.

<Frame>
  <img src="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/apprunner/build.png?fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=bdc3f54a3954bfeacbde8a90a3e75c83" width="800" data-og-width="1672" data-og-height="1466" data-path="img/examples/apprunner/build.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/apprunner/build.png?w=280&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=6d130cb0552af083b47fa257ff042b19 280w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/apprunner/build.png?w=560&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=8504c284a04e2c2c427889927c69b0e9 560w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/apprunner/build.png?w=840&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=bc810f82cc68c21a9c2b82a16f487dac 840w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/apprunner/build.png?w=1100&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=0a0795bca77f664b73e6d1262447a47c 1100w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/apprunner/build.png?w=1650&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=2b7c068eccfbb5ed0d1b92e76259d674 1650w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/apprunner/build.png?w=2500&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=05cecd6d436103f0d41862edfe0f025d 2500w" />
</Frame>

The next page configures your App Runner service. Set a name for your service.
Set your Redis URL that you copied from Upstash console as `REDIS_URL`
environment variable. Your Redis URL should be something like this:
`rediss://:d34baef614b6fsdeb01b25@us1-lasting-panther-33618.upstash.io:33618`
You can leave other settings as default.

<Frame>
  <img src="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/apprunner/config.png?fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=085224000b55e35b2df639faa88d95be" width="800" data-og-width="1680" data-og-height="1842" data-path="img/examples/apprunner/config.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/apprunner/config.png?w=280&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=132ec2c148eece5b4fa59787a319920b 280w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/apprunner/config.png?w=560&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=7cc6bfa0d010c77d4fcf8b31195578f0 560w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/apprunner/config.png?w=840&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=c463380067d8935fd9b0f0d061d0fd9e 840w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/apprunner/config.png?w=1100&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=11b6129f85fc21430e744bb3884dfaf3 1100w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/apprunner/config.png?w=1650&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=e5164cab6f2648590b029f4c98db3f2e 1650w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/apprunner/config.png?w=2500&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=946dbca3821e4f355bb700fff8c02439 2500w" />
</Frame>

Click on `Create and Deploy` at the next page. Your service will be ready in a
few minutes. Click on the default domain, you should see the page with a view
counter as [here](https://xmzuanrpf3.us-east-1.awsapprunner.com/).

### App Runner vs AWS Lambda

* AWS Lambda runs functions, App Runner runs applications. So with App Runner
  you do not need to split your application to functions.
* App Runner is a more portable solution. You can move your application from App
  Runner to any other container service.
* AWS Lambda price scales to zero, App Runner's does not. With App Runner you
  need to pay for an at least one instance unless you pause the system.

App Runner is great alternative when you need more control on your serverless
runtime and application. Check out
[this video](https://www.youtube.com/watch?v=x_1X_4j16A4) to learn more about
App Runner.
