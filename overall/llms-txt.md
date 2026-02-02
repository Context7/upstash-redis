```
### Install Upstash Redis Client via Package Managers

Source: https://upstash.com/docs/redis/sdks/ts/getstarted

Provides installation commands for the Upstash Redis client using popular Node.js package managers: npm, yarn, and pnpm. This allows usage in Node.js environments.

```bash
npm install @upstash/redis
```

```bash
yarn add @upstash/redis
```

```bash
pnpm add @upstash/redis
```

--------------------------------

### Example CMD for Dockerfile

Source: https://upstash.com/docs/redis/tutorials/cloud_run_sessions

This is an example CMD instruction typically found in a Dockerfile. It specifies the command to run when a container is started from the image. In this case, it executes 'npm start', likely to launch a Node.js web server.

```dockerfile
CMD [ "npm", "start" ]
```

--------------------------------

### Install @upstash/ratelimit using npm

Source: https://upstash.com/docs/redis/sdks/ratelimit-ts/gettingstarted

Installs the @upstash/ratelimit package for Node.js projects using npm. This is the first step to integrate rate limiting capabilities.

```bash
npm install @upstash/ratelimit
```

--------------------------------

### Install Django and Upstash Redis Client

Source: https://upstash.com/docs/redis/quickstarts/django

Installs the necessary Python packages for Django and the Upstash Redis client. Ensure you have Python and pip installed.

```shell
pip install django
pip install upstash-redis
```

--------------------------------

### Install Upstash Redis Rate Limiter (Python)

Source: https://upstash.com/docs/redis/sdks/ratelimit-py/gettingstarted

Installs the `upstash-ratelimit` Python package using pip. This is the first step to enable rate limiting functionality in your application.

```bash
pip install upstash-ratelimit
```

--------------------------------

### Install Flask and Upstash Redis Client

Source: https://upstash.com/docs/redis/quickstarts/flask

Installs the necessary Python packages, Flask for web development and upstash-redis for interacting with Upstash Redis.

```shell
pip install flask
pip install upstash-redis
```

--------------------------------

### Node.js Project Setup and Dependency Installation

Source: https://upstash.com/docs/redis/tutorials/aws_app_runner_with_redis

Commands to create a new Node.js project and install the 'ioredis' package, which is required for connecting to Redis.

```bash
npm init
npm install ioredis
```

--------------------------------

### Deploy React Frontend

Source: https://upstash.com/docs/redis/tutorials/cloudflare_websockets_redis

Commands to install dependencies and deploy the React frontend application. This involves navigating to the client directory, installing packages using pnpm, and then deploying using pnpm.

```bash
cd client
pnpm install
pnpm run deploy
```

--------------------------------

### Run Commands with Upstash Redis Client (Python)

Source: https://upstash.com/docs/redis/sdks/py/gettingstarted

Provides examples of executing basic SET and GET commands using both synchronous and asynchronous Upstash Redis clients. It illustrates how to interact with Redis after client initialization.

```python
from upstash_redis import Redis

redis = Redis.from_env()

def main():
  redis.set("a", "b")
  print(redis.get("a"))

# or for async context:

from upstash_redis.asyncio import Redis

redis = Redis.from_env()

async def main():
  await redis.set("a", "b")
  print(await redis.get("a"))
```

--------------------------------

### Copy Example .env File for Upstash Redis

Source: https://upstash.com/docs/redis/quickstarts/supabase

This command copies the example environment file for the Upstash Redis counter function. It ensures that necessary configuration variables are present before proceeding with function setup. No specific inputs or outputs are detailed, but it's a prerequisite for configuring the function.

```shell
cp supabase/functions/upstash-redis-counter/.env.example supabase/functions/upstash-redis-counter/.env
```

--------------------------------

### Run Django Development Server

Source: https://upstash.com/docs/redis/quickstarts/django

Command to start the Django development server. This allows you to test the web application locally.

```shell
python manage.py runserver
```

--------------------------------

### Deploy Cloudflare Worker

Source: https://upstash.com/docs/redis/tutorials/cloudflare_websockets_redis

Commands to install dependencies and deploy the Cloudflare Worker. This involves navigating to the worker directory, installing packages using pnpm, and then deploying using npm.

```bash
cd worker
pnpm install
npm run deploy
```

--------------------------------

### Import Upstash Redis Client in Deno

Source: https://upstash.com/docs/redis/sdks/ts/getstarted

Demonstrates how to import the Upstash Redis client library when using Deno. This is the primary method for Deno projects.

```typescript
import { Redis } from "https://deno.land/x/upstash_redis/mod.ts";
```

--------------------------------

### Manually Configure Upstash Redis Connection

Source: https://upstash.com/docs/redis/sdks/ratelimit-ts/gettingstarted

Demonstrates how to manually instantiate the Redis client by providing the URL and token directly, bypassing the need for environment variables. Useful when connection details are stored differently.

```typescript
new Redis({
  url: "https://****.upstash.io",
  token: "********",
});
```

--------------------------------

### Install Upstash Redis Client (PyPI)

Source: https://upstash.com/docs/redis/sdks/py/gettingstarted

Installs the Upstash Redis client library using pip. This is the first step to using the library in your Python project.

```bash
pip install upstash-redis
```

--------------------------------

### Install isomorphic-fetch for Node.js fetch polyfill

Source: https://upstash.com/docs/redis/sdks/ts/troubleshooting

If running on Node.js v17 or earlier, `fetch` is not natively supported. Install the `isomorphic-fetch` package as a polyfill. This is necessary for platforms that do not provide a built-in polyfill.

```bash
npm i isomorphic-fetch
```

--------------------------------

### Basic Upstash Redis Operations in Node.js

Source: https://upstash.com/docs/redis/sdks/ts/getstarted

Illustrates fundamental operations with the Upstash Redis client in a Node.js environment. It covers initializing the client and performing common Redis commands for strings, sorted sets, lists, hashes, and sets.

```typescript
import { Redis } from "@upstash/redis"

const redis = new Redis({
  url: <UPSTASH_REDIS_REST_URL>,
  token: <UPSTASH_REDIS_REST_TOKEN>,
})

// string
await redis.set('key', 'value');
let data = await redis.get('key');
console.log(data)

await redis.set('key2', 'value2', {ex: 1});

// sorted set
await redis.zadd('scores', { score: 1, member: 'team1' })
data = await redis.zrange('scores', 0, 100 )
console.log(data)

// list
await redis.lpush('elements', 'magnesium')
data = await redis.lrange('elements', 0, 100 )
console.log(data)

// hash
await redis.hset('people', {name: 'joe'})
data = await redis.hget('people', 'name' )
console.log(data)

// sets
await redis.sadd('animals', 'cat')
data  = await redis.spop('animals', 1)
console.log(data)
```

--------------------------------

### Run Flask Application Locally

Source: https://upstash.com/docs/redis/quickstarts/flask

Executes the Flask application from the command line. This command starts the development server, allowing you to access the web application locally.

```shell
python app.py
```

--------------------------------

### Connect to Upstash Redis with phpredis (PHP)

Source: https://upstash.com/docs/redis/howto/connectclient

Demonstrates connecting to Upstash Redis using the phpredis extension in PHP. The example requires endpoint, port, and password for authentication. Basic set and get operations are performed.

```php
<?php

$redis = new Redis();

$redis->connect("YOUR_ENDPOINT", "YOUR_PORT");
$redis->auth("YOUR_PASSWORD");

$redis->set("foo", "bar");

print_r($redis->get("foo"));

```

--------------------------------

### Project Setup: Next.js App Router

Source: https://upstash.com/docs/redis/quickstarts/vercel-functions-app-router

Installs the necessary packages to create a new Next.js application with App Router and the Upstash Redis client.

```shell
npx create-next-app@latest
cd my-app
npm install @upstash/redis
```

--------------------------------

### Import Redis for Cloudflare and Fastly

Source: https://upstash.com/docs/redis/sdks/ratelimit-ts/gettingstarted

Provides alternative import paths for the Redis client from @upstash/redis, specifically tailored for Cloudflare Workers/Pages and Fastly Compute@Edge environments.

```typescript
import { Redis } from "@upstash/redis/cloudflare"; // for cloudflare workers and pages
import { Redis } from "@upstash/redis/fastly"; // for fastly compute@edge
```

--------------------------------

### Create Django Project and App

Source: https://upstash.com/docs/redis/quickstarts/django

Sets up a new Django project and a specific application within that project. This is the foundational structure for the web application.

```shell
django-admin startproject myproject
cd myproject
python manage.py startapp myapp
```

--------------------------------

### Import Ratelimit for Deno

Source: https://upstash.com/docs/redis/sdks/ratelimit-ts/gettingstarted

Imports the Ratelimit class from the @upstash/ratelimit package for Deno projects. This allows for server-side rate limiting in Deno applications.

```typescript
import { Ratelimit } from "https://cdn.skypack.dev/@upstash/ratelimit@latest";
```

--------------------------------

### Node.js Project Dependencies Setup

Source: https://upstash.com/docs/redis/tutorials/cloud_run_sessions

Installs necessary npm packages for an Express.js application, including `express` for the web framework, `redis` for Redis client, `connect-redis` for Redis session store, and `express-session` for session management. This command should be run after initializing a Node.js project.

```bash
npm init

npm install express redis connect-redis express-session
```

--------------------------------

### Run Development Server

Source: https://upstash.com/docs/redis/quickstarts/sst-v2

These commands initiate the development servers for both SST and the Next.js application. First, run `npm run dev` in the project root to start the SST dev server. Then, navigate to the `packages/web` directory and run `npm run dev` to start the Next.js development server. You can then access your application at `http://localhost:3000`.

```shell
npm run dev
cd packages/web
npm run dev
```

--------------------------------

### Install Serverless Framework CLI

Source: https://upstash.com/docs/redis/tutorials/serverless_java_redis

Installs the Serverless Framework globally using npm. This is a prerequisite for deploying serverless applications to AWS.

```shell
npm i serverless@3.39.0 -g
```

--------------------------------

### Connect to Upstash Redis with ioredis (Node.js)

Source: https://upstash.com/docs/redis/howto/connectclient

This example shows how to connect to Upstash Redis using the ioredis library in Node.js. It utilizes a rediss connection string including the password, endpoint, and port. Basic set and get operations are demonstrated.

```javascript
const Redis = require("ioredis");

let client = new Redis("rediss://:YOUR_PASSWORD@YOUR_ENDPOINT:YOUR_PORT");
await client.set("foo", "bar");
let x = await client.get("foo");
console.log(x);
```

--------------------------------

### Implement Ratelimit with Upstash Redis

Source: https://upstash.com/docs/redis/sdks/ratelimit-ts/gettingstarted

Initializes and uses the Ratelimit class with an Upstash Redis instance. It demonstrates how to configure a sliding window limiter and apply it to requests. Assumes Redis connection details are available via environment variables.

```typescript
import { Ratelimit } from "@upstash/ratelimit"; // for deno: see above
import { Redis } from "@upstash/redis";

// Create a new ratelimiter, that allows 10 requests per 10 seconds
const ratelimit = new Ratelimit({
  redis: Redis.fromEnv(),
  limiter: Ratelimit.slidingWindow(10, "10 s"),
  analytics: true,
  /**
   * Optional prefix for the keys used in redis. This is useful if you want to share a redis
   * instance with other applications and want to avoid key collisions. The default prefix is
   * "@upstash/ratelimit"
   */
  prefix: "@upstash/ratelimit",
});

// Use a constant string to limit all requests with a single ratelimit
// Or use a userID, apiKey or ip address for individual limits.
const identifier = "api";
const { success } = await ratelimit.limit(identifier);

if (!success) {
  return "Unable to process at this time";
}
doExpensiveCalculation();
return "Here you go!";
```

--------------------------------

### Connect to Upstash Redis with Jedis (Java)

Source: https://upstash.com/docs/redis/howto/connectclient

Example of connecting to Upstash Redis using the Jedis library in Java. It requires endpoint, port, and password for authentication, with TLS enabled by default. Basic set and get operations are shown.

```java
Jedis jedis = new Jedis("YOUR_ENDPOINT", "YOUR_PORT", true);
jedis.auth("YOUR_PASSWORD");
jedis.set("foo", "bar");
String value = jedis.get("foo");
System.out.println(value);
```

--------------------------------

### Python BITPOS Example - Find First Set/Clear Bit

Source: https://upstash.com/docs/redis/sdks/py/commands/bitmap/bitpos

Demonstrates how to use the BITPOS command in Python to find the index of the first set (1) or clear (0) bit within a Redis string. Includes examples with and without specifying start and end ranges. Assumes a Redis client connection is established.

```python
redis.setbit("mykey", 7, 1)
redis.setbit("mykey", 8, 1)

assert redis.bitpos("mykey", 1) == 7
assert redis.bitpos("mykey", 0) == 0

# With a range
assert redis.bitpos("mykey", 1, 0, 2) == 0
assert redis.bitpos("mykey", 1, 2, 3) == -1
```

```python
redis.bitpos("key", 1, 5, 20)
```

--------------------------------

### Install Project Dependencies

Source: https://upstash.com/docs/redis/tutorials/using_serverless_framework

Installs all the dependencies listed in the package.json file. This command ensures that the `@upstash/redis` library and other necessary packages are available for the project.

```shell
npm install

```

--------------------------------

### Node.js Package.json Start Script

Source: https://upstash.com/docs/redis/tutorials/cloud_run_sessions

Defines the 'start' script in a Node.js project's `package.json` file. This script is used to run the application using the `node` command, typically specified as `node index` to execute the main application file.

```json
{
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "node index"
  }
}
```

--------------------------------

### Serverless Project Setup with Node.js

Source: https://upstash.com/docs/redis/tutorials/histogram

Initializes a new serverless project for AWS Node.js. This involves using the Serverless Framework CLI to create the project structure and then setting up a Node.js project within the created folder. Dependencies like 'ioredis' for Redis interaction and 'hdr-histogram-js' for histogram functionality are installed via npm.

```text
>> serverless

Serverless: No project detected. Do you want to create a new one? Yes
Serverless: What do you want to make? AWS Node.js
Serverless: What do you want to call this project? histogram-api

Project successfully created in 'histogram-api' folder.

You can monitor, troubleshoot, and test your new service with a free Serverless account.

Serverless: Would you like to enable this? No
You can run the “serverless” command again if you change your mind later.
```

```bash
npm init
npm install ioredis
npm install hdr-histogram-js
```

--------------------------------

### Initialize Fastly Compute Project (JavaScript)

Source: https://upstash.com/docs/redis/quickstarts/fastlycompute

This snippet demonstrates the command-line interaction for initializing a new Fastly Compute@Edge project using JavaScript and an empty starter kit. It guides the user through selecting the language and starter template.

```shell
> fastly compute init

Creating a new Compute@Edge project.

Press ^C at any time to quit.

Name: [fastly-upstash]
Description: 
Author: [enes@upstash.com]
Language:
[1] Rust
[2] JavaScript
[3] AssemblyScript (beta)
[4] Other ('bring your own' Wasm binary)
Choose option: [1] 2
Starter kit:
[1] Default starter for JavaScript
    A basic starter kit that demonstrates routing, simple synthetic responses and
    overriding caching rules.
    https://github.com/fastly/compute-starter-kit-javascript-default
[2] Empty starter for JavaScript
    An empty application template for the Fastly Compute@Edge environment which simply
    returns a 200 OK response.
    https://github.com/fastly/compute-starter-kit-javascript-empty
Choose option or paste git URL: [1] 2
```

--------------------------------

### Install Project Dependencies

Source: https://upstash.com/docs/redis/tutorials/rate-limiting

Installs all the dependencies listed in the `package.json` file for the project, including Upstash libraries.

```shell
npm install
```

--------------------------------

### Project Initialization with Next.js and SST

Source: https://upstash.com/docs/redis/quickstarts/ion

Commands to create a new Next.js application and initialize SST within it. Ensure you have Node.js and npm installed, and AWS credentials configured.

```shell
npx create-next-app@latest
cd my-app
sst init
```

--------------------------------

### Create Django Project for Vercel

Source: https://upstash.com/docs/redis/quickstarts/vercel-python-runtime

Initializes a new Django project using a Vercel template, preparing it for deployment. This command clones a specific example from the Vercel GitHub repository.

```shell
npx create-next-app vercel-django --example "https://github.com/vercel/examples/tree/python/django"
cd vercel-django
```

--------------------------------

### Launch Phoenix App on Fly

Source: https://upstash.com/docs/redis/quickstarts/elixir

This command initiates the deployment process for a Phoenix application on Fly.io. It detects the application type and prompts for configuration settings. Ensure Fly CLI is installed and authenticated before running. The command may automatically add environment variables like `REDIS_URL` if not already set.

```bash
fly launch
```

--------------------------------

### Install Upstash Ratelimit Strapi Plugin

Source: https://upstash.com/docs/redis/integrations/ratelimit/strapi/getting-started

Install the Upstash Ratelimit Strapi plugin using either npm or yarn. This package is essential for enabling rate limiting features within your Strapi application.

```bash
npm install --save @upstash/strapi-plugin-upstash-ratelimit
```

```bash
yarn add @upstash/strapi-plugin-upstash-ratelimit
```

--------------------------------

### Install Serverless Framework

Source: https://upstash.com/docs/redis/tutorials/rate-limiting

Installs the Serverless Framework globally using npm, which is a prerequisite for managing and deploying serverless applications.

```shell
npm i serverless -g
```

--------------------------------

### Create New Laravel Project using Laravel CLI

Source: https://upstash.com/docs/redis/quickstarts/laravel

Creates a new Laravel project named 'example-app' using the globally installed Laravel CLI and navigates into the project directory. Requires Laravel installer to be set up first.

```shell
laravel new example-app
cd example-app
```

--------------------------------

### Install Node.js dependencies for Upstash and Express

Source: https://upstash.com/docs/redis/quickstarts/koyeb

Installs the necessary Node.js packages: `@upstash/redis` for database connectivity and `express` for building the web application.

```bash
npm install @upstash/redis express
```

--------------------------------

### Initialize Nuxt.js Project

Source: https://upstash.com/docs/redis/tutorials/nuxtjs_with_redis

Command to create a new Nuxt.js project using the Nuxt CLI. After creation, dependencies including '@upstash/redis' need to be installed.

```bash
npx nuxi@latest init nuxtjs-with-redis
npm install @upstash/redis
```

--------------------------------

### Install Toast Component for React

Source: https://upstash.com/docs/redis/tutorials/notification

NPM command to install the 'react-toastify' package, which is used for displaying notification messages to the user in a React application.

```shell
npm install --save react-toastify
```

--------------------------------

### Upstash Redis LPUSHX Python Example

Source: https://upstash.com/docs/redis/sdks/py/commands/list/lpushx

Demonstrates the usage of the LPUSHX command in Python with Upstash Redis. It shows how to push elements to an existing list and how the command behaves when the list does not exist. Assumes a Redis client instance is available.

```python
redis.lpush("mylist", "one")

assert redis.lpushx("mylist", "two", "three") == 3

assert lrange("mylist", 0, -1) == ["three", "two", "one"]

# Non existing key
assert redis.lpushx("non-existent-list", "one") == 0
```

--------------------------------

### Get String Length with Redis STRLEN (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/string/strlen

Demonstrates how to use the STRLEN command in Redis to get the length of a string value. This example assumes you have a Redis client instance named 'redis' available and have already set a key with a string value.

```typescript
await redis.set("key", "helloworld")
const length = await redis.strlen("key");
console.log(length); // 10
```

--------------------------------

### Install FastAPI and Upstash Redis

Source: https://upstash.com/docs/redis/quickstarts/fastapi

Installs the required Python libraries for FastAPI and Upstash Redis. Ensure you have Python and pip installed.

```shell
pip install fastapi
pip install upstash-redis
```

--------------------------------

### Get Multiple Bitfield Values in Python

Source: https://upstash.com/docs/redis/sdks/py/commands/bitmap/bitfield

This example shows how to retrieve values from a Redis bitfield at specified offsets. It sets an initial byte string and then uses the `get` operation to fetch the unsigned 8-bit integers at offsets 0, 8, and 16, returning their values.

```python
redis.set("mykey", "\x05\x06\x07")

result = redis.bitfield("mykey") \
    .get("u8", 0) \
    .get("u8", 8) \
    .get("u8", 16) \
    .execute()

assert result == [5, 6, 7]
```

--------------------------------

### Install Chat App Dependencies (Bash)

Source: https://upstash.com/docs/redis/tutorials/python_realtime_chat

Installs the necessary Python libraries for building the real-time chat application, including Flask for the web framework, Flask-SocketIO for WebSocket communication, and the Redis library for interacting with the Redis database.

```bash
pip install flask flask-socketio redis
```

--------------------------------

### Python GETRANGE Example with Upstash Redis

Source: https://upstash.com/docs/redis/sdks/py/commands/string/getrange

This Python code snippet demonstrates how to use the GETRANGE command with Upstash Redis. It first sets a key-value pair and then retrieves a substring from the value. This requires the 'redis' library to be installed.

```python
redis.set("key", "Hello World")

assert redis.getrange("key", 0, 4) == "Hello"
```

--------------------------------

### Install upstash-redis via npm

Source: https://upstash.com/docs/redis/howto/connectwithupstashredis

Installs the upstash-redis JavaScript package using npm. This is the first step to integrating Upstash Redis into your project.

```bash
npm install @upstash/redis
```

--------------------------------

### Retrieve List Element by Index with Python

Source: https://upstash.com/docs/redis/sdks/py/commands/list/lindex

Demonstrates how to use the `lindex` command in Python to fetch an element from a Redis list. It first pushes elements to a list and then retrieves the element at index 0. This example requires the `redis` library to be installed.

```python
redis.rpush("key", "a", "b", "c")

assert redis.lindex("key", 0) == "a"
```

--------------------------------

### Read Data from Upstash Redis in Next.js Server Component

Source: https://upstash.com/docs/redis/quickstarts/nextjs-app-router

Demonstrates how to fetch data from Upstash Redis within a Next.js server component. It retrieves a value associated with the key 'count' and displays it. This example assumes the `redis` client has been initialized.

```typescript
import { redis } from "@/lib/redis"

// 👇 server component
const Page = async () => {
  const count = await redis.get<number>("count")
  return <p>count: {count}</p>
}

export default Page
```

--------------------------------

### Handle Serverless Runtimes with waitUntil

Source: https://upstash.com/docs/redis/sdks/ratelimit-ts/gettingstarted

Ensures asynchronous operations like MultiRegion synchronization or analytics reporting complete before the serverless function runtime ends. It utilizes the `pending` promise returned by `ratelimit.limit()` and passes it to `context.waitUntil()`.

```typescript
const { pending } = await ratelimit.limit("id");
context.waitUntil(pending);
```

--------------------------------

### Add npm Run Scripts for Development and Production

Source: https://upstash.com/docs/redis/quickstarts/koyeb

This `package.json` snippet adds 'dev' and 'start' scripts to manage the Node.js application. The 'dev' script enables debug logging for Express, while 'start' runs the application normally. These scripts are essential for local development and deployment.

```json
{
  "name": "example-koyeb-upstash",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "dev": "DEBUG=express:* node index.js",
    "start": "node index.js",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "@upstash/redis": "^1.20.6",
    "express": "^4.18.2"
  }
}
```

--------------------------------

### Start Local Development Server

Source: https://upstash.com/docs/redis/tutorials/using_serverless_framework

Starts the Serverless Framework's local development server. This allows for testing the Lambda function and API locally before deploying to AWS.

```shell
serverless dev

```

--------------------------------

### Create SST + Next.js App

Source: https://upstash.com/docs/redis/quickstarts/sst-v2

This command initializes a new project using SST with a standard Next.js template. It sets up the basic structure for your application. After execution, navigate into the created directory and install npm dependencies.

```shell
npx create-sst@latest --template standard/nextjs
cd my-sst-app
npm install
```

--------------------------------

### Install Laravel Installer

Source: https://upstash.com/docs/redis/quickstarts/laravel

Installs the Laravel Command Line Interface globally using Composer. This is a prerequisite for creating new Laravel projects using the 'laravel new' command.

```shell
composer global require laravel/installer
```

--------------------------------

### Connect and Interact with Upstash Redis using Go and Redigo

Source: https://upstash.com/docs/redis/howto/connectclient

This Go code snippet demonstrates how to connect to Upstash Redis using the redigo library. It includes steps for dialing the Redis server with TLS, authenticating using a password, and performing SET and GET operations. Ensure you replace 'YOUR_ENDPOINT', 'YOUR_PORT', and 'YOUR_PASSWORD' with your actual Upstash Redis credentials.

```go
func main() {
  c, err := redis.Dial("tcp", "YOUR_ENDPOINT:YOUR_PORT", redis.DialUseTLS(true))
  if err != nil {
      panic(err)
  }

  _, err = c.Do("AUTH", "YOUR_PASSWORD")
  if err != nil {
      panic(err)
  }

  _, err = c.Do("SET", "foo", "bar")
  if err != nil {
      panic(err)
  }

  value, err := redis.String(c.Do("GET", "foo"))
  if err != nil {
      panic(err)
  }

  println(value)
}
```

--------------------------------

### Apply Rate Limit Using IP Address (JSON)

Source: https://upstash.com/docs/redis/integrations/ratelimit/strapi/configurations

This example configures rate limiting based on the client's IP address. It applies a fixed-window limit of 10 tokens per 20 seconds to all routes for incoming GET and POST requests. The identifier source is set to 'ip'.

```json
{
  "strapi-plugin-upstash-ratelimit": {
    "enabled": true,
    "resolve": "./src/plugins/strapi-plugin-upstash-ratelimit",
    "config": {
      "enabled": true,
      "token": "process.env.UPSTASH_REDIS_REST_TOKEN",
      "url": "process.env.UPSTASH_REDIS_REST_URL",
      "strategy": [
        {
          "methods": ["GET", "POST"],
          "path": "*",
          "identifierSource": "ip",
          "limiter": {
            "algorithm": "fixed-window",
            "tokens": 10,
            "window": "20s"
          }
        }
      ],
      "prefix": "@strapi"
    }
  }
}
```

--------------------------------

### Import isomorphic-fetch for Node.js fetch polyfill

Source: https://upstash.com/docs/redis/sdks/ts/troubleshooting

After installing `isomorphic-fetch`, import it in your TypeScript project to enable the `fetch` API. This allows the Upstash Redis client to make network requests when running in Node.js environments without native `fetch` support.

```typescript
import { Redis } from "@upstash/redis";
import "isomorphic-fetch";

const redis = new Redis({
  /*...*/
});
```

--------------------------------

### Implement Rate Limiting with Upstash Redis (Python)

Source: https://upstash.com/docs/redis/sdks/ratelimit-py/gettingstarted

Demonstrates how to create and use a rate limiter with Upstash Redis in Python. It shows initializing `Ratelimit` with `Redis.from_env()` and `FixedWindow`, and how to check if a request is allowed using an identifier.

```python
from upstash_ratelimit import Ratelimit, FixedWindow
from upstash_redis import Redis

# Create a new ratelimiter, that allows 10 requests per 10 seconds
ratelimit = Ratelimit(
    redis=Redis.from_env(),
    limiter=FixedWindow(max_requests=10, window=10),
    # Optional prefix for the keys used in Redis. This is useful
    # if you want to share a Redis instance with other applications
    # and want to avoid key collisions. The default prefix is
    # "@upstash/ratelimit"
    prefix="@upstash/ratelimit",
)

# Use a constant string to limit all requests with a single ratelimit
# Or use a user ID, API key or IP address for individual limits.
identifier = "api"
response = ratelimit.limit(identifier)

if not response.allowed:
    print("Unable to process at this time")
else:
    do_expensive_calculation()
    print("Here you go!")
```

--------------------------------

### RPUSHX Example in Python

Source: https://upstash.com/docs/redis/sdks/py/commands/list/rpushx

Demonstrates the usage of the RPUSHX command in Python. It shows how to push multiple elements to an existing list and verifies the list's content. It also illustrates the behavior when attempting to push to a non-existent list.

```python
assert redis.rpushx("mylist", "one", "two", "three") == 3

assert lrange("mylist", 0, -1) == ["one", "two", "three"]

# Non existing key
assert redis.rpushx("non-existent-list", "one") == 0
```

--------------------------------

### Install BullMQ and Upstash Redis

Source: https://upstash.com/docs/redis/integrations/bullmq

Installs the necessary packages for using BullMQ with Upstash Redis. This command assumes you have Node.js and npm installed.

```bash
npm install bullmq upstash-redis
```

--------------------------------

### Start Development Server

Source: https://upstash.com/docs/redis/tutorials/rate-limiting

Starts the Serverless Framework development server, allowing for local testing and debugging of the deployed serverless functions.

```shell
serverless dev
```

--------------------------------

### Navigate to Project Directory

Source: https://upstash.com/docs/redis/tutorials/using_serverless_framework

Changes the current directory to the newly created Serverless Framework project. This is a standard navigation step before installing dependencies or modifying project files.

```shell
cd counter-serverless

```

--------------------------------

### Install and Use upstash-redis-dump Tool

Source: https://upstash.com/docs/redis/howto/migratefromregionaltoglobal

This snippet demonstrates how to install the `upstash-redis-dump` Go tool and use it to export data from a regional Redis database and import it into a global database. Ensure you have Go installed. The export command creates a dump file, and the import command uses `redis-cli` to pipe the dump file into the destination database.

```bash
go install github.com/upstash/upstash-redis-dump@latest
```

```bash
upstash-redis-dump -db 0 -host YOUR_REGIONAL_HOST -port YOUR_DATABASE_PORT -pass YOUR_PASSWORD -tls > redis.dump
```

```bash
redis-cli --tls -u redis://YOUR_PASSWORD@YOUR_REGIONAL_HOST:6379 --pipe < redis.dump
```

--------------------------------

### Get JSON Value with Upstash Redis Client (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/json/get

Demonstrates how to retrieve a value from a JSON document stored in Upstash Redis using the client library. This example shows the basic usage with a key and a JSON path.

```typescript
const value = await redis.json.get("key", "$.path.to.somewhere");
```

--------------------------------

### HSCAN with Field Matching in TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/hash/hscan

Illustrates how to use the 'match' option with HSCAN to filter hash fields based on a glob-style pattern. This example sets hash fields and then performs an HSCAN, requesting only fields that start with 'user'.

```typescript
await redis.hset("key", {
    id: 1,
    username: "chronark",
    name: "andreas",
  });
  const [newCursor, fields] = await redis.hscan("key", 0, { match: "user*" });
  console.log(newCursor); // likely `0` since this is a very small hash
  console.log(fields); // ["username", "chronark"]
```

--------------------------------

### Project Setup: Initialize CDK App (TypeScript)

Source: https://upstash.com/docs/redis/quickstarts/python-aws-lambda

Initializes a new AWS CDK project with TypeScript as the language. This command sets up the basic directory structure and configuration files for a CDK application.

```shell
cdk init app --language typescript
```

--------------------------------

### Run Supabase Function Locally

Source: https://upstash.com/docs/redis/quickstarts/supabase

These commands initiate the local Supabase environment and serve the 'upstash-redis-counter' function. `supabase start` brings up local services, and `supabase functions serve` runs the specified function, optionally using an environment file for configuration. This allows for local testing before deployment.

```bash
supabase start
supabase functions serve upstash-redis-counter --no-verify-jwt --env-file supabase/functions/upstash-redis-counter/.env
```

--------------------------------

### Install Dependencies for FastAPI Rate Limiting

Source: https://upstash.com/docs/redis/tutorials/python_rate_limiting

Installs necessary Python packages including FastAPI, the Upstash Redis client, the Upstash rate limiting package, and an ASGI server like Uvicorn. These are essential for building and running the rate-limited application.

```shell
pip install fastapi upstash-redis upstash-ratelimit uvicorn[standard]
```

--------------------------------

### Fastly Redis Client Setup

Source: https://upstash.com/docs/redis/sdks/ts/deployment

Sets up the Upstash Redis client for use with Fastly. This requires configuring a backend in `fastly.toml`. The client is instantiated with URL, token, and the backend name.

```typescript
import { Redis } from "@upstash/redis/fastly"

const redis = new Redis({
  url: <UPSTASH_REDIS_REST_URL>,
  token: <UPSTASH_REDIS_REST_TOKEN>,
  backend: <BACKEND_NAME>,
})
```

--------------------------------

### Initialize npm project

Source: https://upstash.com/docs/redis/quickstarts/koyeb

Initializes a new Node.js project by creating a package.json file with default settings.

```bash
npm init -y
```

--------------------------------

### Testing Leaderboard API with cURL (Shell)

Source: https://upstash.com/docs/redis/tutorials/edge_leaderboard

These shell commands demonstrate how to test the leaderboard API locally using cURL. They show examples for adding new scores via POST requests and retrieving the leaderboard via GET requests, including latency measurement.

```shell
curl -X POST http://127.0.0.1:8787\?player\=messi\&score\=13

curl -X POST http://127.0.0.1:8787\?player\=ronaldo\&score\=17

curl -X POST http://127.0.0.1:8787\?player\=benzema\&score\=18
```

```shell
curl -w '\n Latency: %{time_total}s\n' http://127.0.0.1:8787
```

--------------------------------

### Connect to Upstash Redis with redis-py (Python)

Source: https://upstash.com/docs/redis/howto/connectclient

Connect to Upstash Redis using the redis-py library in Python. This example requires the host, port, password, and explicitly enables SSL. It demonstrates setting and retrieving a value.

```python
import redis
r = redis.Redis(
 host= 'YOUR_ENDPOINT',
 port= 'YOUR_PORT',
 password= 'YOUR_PASSWORD',
 ssl=True)
r.set('foo','bar')
print(r.get('foo'))
```

--------------------------------

### Install Python Libraries for Web Scraping and Redis

Source: https://upstash.com/docs/redis/tutorials/python_multithreading

Install the required Python libraries: threading for multithreading, requests for making HTTP requests, upstash-redis for Redis interaction, and python-dotenv for loading environment variables.

```bash
pip install threading requests upstash-redis python-dotenv
```

--------------------------------

### Create Serverless Framework Project

Source: https://upstash.com/docs/redis/tutorials/using_serverless_framework

Initializes a new Serverless Framework project for AWS and Node.js. This command sets up the basic structure for a serverless application.

```shell
➜  tutorials > ✗ serverless
Serverless ϟ Framework

Welcome to Serverless Framework V.4

Create a new project by selecting a Template to generate scaffolding for a specific use-case.

✔ Select A Template: · AWS / Node.js / HTTP API

✔ Name Your Project: · counter-serverless

✔ Template Downloaded

✔ Create Or Select An Existing App: · Create A New App

✔ Name Your New App: · counter-serverless

Your new Service "counter-serverless" is ready. Here are next steps:

• Open Service Directory: cd counter-serverless
• Install Dependencies: npm install (or use another package manager)
• Deploy Your Service: serverless deploy

```

--------------------------------

### Set Upstash Redis Environment Variables

Source: https://upstash.com/docs/redis/quickstarts/django

Exports the Upstash Redis URL and token as environment variables. These are required for the Upstash Redis client to connect to your database.

```shell
export UPSTASH_REDIS_REST_URL=<YOUR_URL>
export UPSTASH_REDIS_REST_TOKEN=<YOUR_TOKEN>
```

--------------------------------

### Install Dependencies for FastAPI and Upstash Redis

Source: https://upstash.com/docs/redis/tutorials/python_fastapi_caching

Installs the necessary Python packages for building a FastAPI application with Upstash Redis caching. This includes the FastAPI framework, the Upstash Redis client, and Uvicorn for running the ASGI application.

```shell
pip install fastapi upstash-redis uvicorn[standard]
```

--------------------------------

### Function Setup: Increment Redis Counter with Upstash Redis

Source: https://upstash.com/docs/redis/quickstarts/vercel-functions-pages-router

Implements a Vercel Serverless Function (`/pages/api/hello.ts`) to increment a Redis counter using the Upstash Redis client. It initializes the Redis client from environment variables and uses the `incr` command. The function returns the updated counter value.

```typescript
import { Redis } from "@upstash/redis";
import type { NextApiRequest, NextApiResponse } from "next";

const redis = Redis.fromEnv();

export default async function handler(
  req: NextApiRequest,
  res: NextApiResponse,
) {
  const count = await redis.incr("counter");
  res.status(200).json({ count });
}
```

--------------------------------

### Create and navigate to demo application directory

Source: https://upstash.com/docs/redis/quickstarts/koyeb

Shell commands to create a new directory for the demo application and change the current directory into it.

```bash
mkdir example-koyeb-upstash
cd example-koyeb-upstash
```

--------------------------------

### Get All Hash Values (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/hash/hvals

Retrieves all values from a hash stored at the specified key using the Upstash Redis client. This example first sets fields and values in a hash, then retrieves all associated values. It requires the Upstash Redis client library.

```typescript
await redis.hset("key", {
  field1: "Hello",
  field2: "World",
})
const values = await redis.hvals("key")
console.log(values) // ["Hello", "World"]
```

--------------------------------

### Create New Laravel Project using Composer

Source: https://upstash.com/docs/redis/quickstarts/laravel

Creates a new Laravel project named 'example-app' directly using Composer, bypassing the need for the global Laravel installer. It then navigates into the project directory.

```shell
composer create-project laravel/laravel example-app
cd example-app
```

--------------------------------

### Python ZLEXCOUNT Example - Upstash Redis

Source: https://upstash.com/docs/redis/sdks/py/commands/zset/zlexcount

This Python snippet demonstrates how to use the ZLEXCOUNT command with Upstash Redis. It first adds elements to a sorted set and then uses ZLEXCOUNT to count elements within the entire lexicographical range ('-' to '+'). This function requires the 'redis' library to be installed and configured for Upstash.

```python
redis.zadd("myset", {"a": 1, "b": 2, "c": 3})

assert redis.zlexcount("myset", "-", "+") == 3
```

--------------------------------

### Initialize AWS SAM Application

Source: https://upstash.com/docs/redis/tutorials/using_aws_sam

This snippet shows the interactive process of initializing a new AWS SAM application. It guides the user through selecting a template and configuring runtime options, X-Ray tracing, CloudWatch Application Insights, and structured logging.

```shell
➜  tutorials > ✗ sam init
Which template source would you like to use?
	1 - AWS Quick Start Templates
	2 - Custom Template Location
Choice: 1

Choose an AWS Quick Start application template
	1 - Hello World Example
	2 - Data processing
	3 - Hello World Example with Powertools for AWS Lambda
	4 - Multi-step workflow
	5 - Scheduled task
	6 - Standalone function
	7 - Serverless API
	8 - Infrastructure event management
	9 - Lambda Response Streaming
	10 - Serverless Connector Hello World Example
	11 - Multi-step workflow with Connectors
	12 - GraphQLApi Hello World Example
	13 - Full Stack
	14 - Lambda EFS example
	15 - DynamoDB Example
	16 - Machine Learning
Template: 1

Use the most popular runtime and package type? (Python and zip) [y/N]: y

Would you like to enable X-Ray tracing on the function(s) in your application?  [y/N]: N

Would you like to enable monitoring using CloudWatch Application Insights?
For more info, please view https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch-application-insights.html [y/N]: N

Would you like to set Structured Logging in JSON format on your Lambda functions?  [y/N]: N
```

--------------------------------

### Python Redis ZRANGE Examples

Source: https://upstash.com/docs/redis/sdks/py/commands/zset/zrange

Demonstrates various ways to use the ZRANGE command in Python with the Upstash Redis client. Includes examples for basic range retrieval, reversing order, sorting by score, and including scores in the response.

```python
redis.zadd("myset", {"a": 1, "b": 2, "c": 3})

assert redis.zrange("myset", 0, 1) == ["a", "b"]
```

```python
redis.zadd("myset", {"a": 1, "b": 2, "c": 3})

assert redis.zrange("myset", 0, 1, rev=True) == ["c", "b"]
```

```python
redis.zadd("myset", {"a": 1, "b": 2, "c": 3})

assert redis.zrange("myset", 0, 1, sortby="BYSCORE") == ["a", "b"]
```

```python
redis.zadd("myset", {"a": 1, "b": 2, "c": 3})

assert redis.zrange("myset", 0, 1, withscores=True) == [("a", 1), ("b", 2)]
```

--------------------------------

### Create Directory and Navigate

Source: https://upstash.com/docs/redis/tutorials/api_with_cdk

Shell command to create a new directory for the CDK project and navigate into it. This sets up the foundational directory structure.

```shell
mkdir counter-cdk && cd counter-cdk
```

--------------------------------

### Set and get data with Upstash Redis

Source: https://upstash.com/docs/redis/sdks/ts/troubleshooting

This TypeScript snippet demonstrates setting a string value ('value') to a key ('key') and then retrieving it using the Upstash Redis client. The output shows the base64 encoded value if response encoding is enabled by default.

```typescript
await redis.set("key", "value");
const data = await redis.get("key");
console.log(data);

// dmFsdWU=
```

--------------------------------

### Get JSON Value Type with TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/json/type

This TypeScript example demonstrates how to use the JSON.TYPE command with Upstash Redis to retrieve the type of a JSON value. It requires the 'redis' client instance and specifies the key and path to the JSON element.

```typescript
const myType = await redis.json.type("key", "$.path.to.value");
```

--------------------------------

### Get Set Difference (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/zset/zdiff

Calculates the difference between two sets stored in Redis using the ZDIFF command. It returns a list of elements present in the first set but not in the second. This example demonstrates the basic usage without scores.

```python
redis.zadd("key1", {"a": 1, "b": 2, "c": 3})

redis.zadd("key2", {"c": 3, "d": 4, "e": 5})

result = redis.zdiff(["key1", "key2"])

assert result == ["a", "b"]
```

--------------------------------

### Initialize Upstash Redis Client (Python)

Source: https://upstash.com/docs/redis/sdks/py/gettingstarted

Demonstrates how to initialize both synchronous and asynchronous Upstash Redis clients using direct URL and token credentials. Ensure you replace placeholders with your actual Upstash credentials.

```python
# for sync client
from upstash_redis import Redis

redis = Redis(url="UPSTASH_REDIS_REST_URL", token="UPSTASH_REDIS_REST_TOKEN")

# for async client
from upstash_redis.asyncio import Redis

redis = Redis(url="UPSTASH_REDIS_REST_URL", token="UPSTASH_REDIS_REST_TOKEN")
```

--------------------------------

### Use Laravel Cache with Redis

Source: https://upstash.com/docs/redis/quickstarts/laravel

Utilizes Laravel's Cache facade to put and get values, leveraging the previously configured Upstash Redis cache store. This example shows storing a value with an expiration time and then retrieving it.

```php
Cache::put('key', 'value', now()->addMinutes(10));
$value = Cache::get('key');
```

--------------------------------

### Python Example: Upstash Redis HSETNX

Source: https://upstash.com/docs/redis/sdks/py/commands/hash/hsetnx

Demonstrates the usage of the HSETNX command in Python with Upstash Redis. It shows how to set a new field and attempts to set an existing field, illustrating the boolean return values.

```python
assert redis.hsetnx("myhash", "field1", "Hello") == True
assert redis.hsetnx("myhash", "field1", "World") == False
```

--------------------------------

### Initialize Koyeb App with Upstash Redis

Source: https://upstash.com/docs/redis/quickstarts/koyeb

Initializes a new Koyeb application from a GitHub repository and configures environment variables for Upstash Redis connection. Requires replacing placeholders with actual values.

```bash
koyeb app init example-koyeb-upstash \
  --git github.com/<YOUR_GITHUB_USERNAME>/<YOUR_REPOSITORY_NAME> \
  --git-branch main \
  --ports 3000:http \
  --routes /:3000 \
  --env PORT=3000 \
  --env UPSTASH_REDIS_REST_URL="<YOUR_UPSTASH_REDIS_REST_URL>" \
  --env UPSTASH_REDIS_REST_TOKEN="<YOUR_UPSTASH_REDIS_REST_TOKEN>"
```

--------------------------------

### Get Millisecond TTL for Hash Fields with HPTTL (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/hash/hpttl

This example demonstrates how to use the HPTTL command to retrieve the remaining time-to-live in milliseconds for specified fields within a Redis hash. It assumes the Upstash Redis client is initialized and available as 'redis'.

```typescript
await redis.hset("my-key", "my-field", "my-value");
await redis.hpexpire("my-key", "my-field", 1000);
const ttl = await redis.hpttl("my-key", "my-field");

console.log(ttl); // e.g., [950]
```

--------------------------------

### Install Celery with Redis Support

Source: https://upstash.com/docs/redis/integrations/celery

Installs the Celery library with the necessary Redis integration package. This is a prerequisite for using Celery with Redis as a broker or backend.

```bash
pip install "celery[redis]"
```

--------------------------------

### Get and Set Key Value with Upstash Redis (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/string/getset

This TypeScript example demonstrates how to use the GETSET command with Upstash Redis. It retrieves the existing value associated with a given key and simultaneously sets a new value for that key. The function returns the old value of the key, or null if the key did not exist.

```typescript
const oldValue = await redis.getset("key", newValue);

```

--------------------------------

### Install Laravel API Package

Source: https://upstash.com/docs/redis/tutorials/laravel_caching

Installs the necessary package for building API resources within your Laravel application. This command prepares your project for API development.

```shell
php artisan install:api
```

--------------------------------

### Create Upstash Redis Client Instance in Next.js

Source: https://upstash.com/docs/redis/quickstarts/nextjs-app-router

Initializes a new Redis client instance using the environment variables for URL and token. This `redis` client can then be imported and used in server components or API routes for Upstash Redis operations.

```typescript
import { Redis } from "@upstash/redis"

// 👇 we can now import our redis client anywhere we need it
export const redis = new Redis({
  url: process.env.UPSTASH_REDIS_REST_URL,
  token: process.env.UPSTASH_REDIS_REST_TOKEN,
})
```

--------------------------------

### Python Example: Using ZRANDMEMBER in Upstash Redis

Source: https://upstash.com/docs/redis/sdks/py/commands/zset/zrandmember

This Python snippet demonstrates how to use the ZRANDMEMBER command with Upstash Redis. It shows adding members to a sorted set and then retrieving single or multiple random members, with and without scores. Ensure the 'redis' library is installed and configured to connect to your Upstash Redis instance.

```python
redis.zadd("myset", {"one": 1, "two": 2, "three": 3})

# "one"
redis.zrandmember("myset")

# ["one", "three"]
redis.zrandmember("myset", 2)
```

--------------------------------

### TypeScript Rate Limiting - Basic Usage

Source: https://context7.com/context7/upstash-redis/llms.txt

This TypeScript code sets up basic rate limiting using the `@upstash/ratelimit` library. It demonstrates creating a rate limiter with the sliding window algorithm and checking rate limits for individual users. Ensure `@upstash/redis` and `@upstash/ratelimit` are installed (`npm install @upstash/redis @upstash/ratelimit`).

```typescript
import { Ratelimit } from "@upstash/ratelimit";
import { Redis } from "@upstash/redis";

// Create rate limiter with sliding window algorithm
const ratelimit = new Ratelimit({
  redis: Redis.fromEnv(),
  limiter: Ratelimit.slidingWindow(10, "10 s"), // 10 requests per 10 seconds
  analytics: true,
  prefix: "@upstash/ratelimit",
});

// Check rate limit per user/API key/IP
async function handleRequest(userId: string) {
  const { success, limit, remaining, reset } = await ratelimit.limit(userId);

  if (!success) {
    return {
      error: "Rate limit exceeded",
      retryAfter: Math.floor((reset - Date.now()) / 1000),
      remaining: 0,
    };
  }

  // Process request
  const result = await expensiveOperation();

  return {
    data: result,
    rateLimit: {
      limit,
      remaining,
      reset: new Date(reset).toISOString(),
    },
  };
}

// Different algorithms for different use cases
const fixedWindow = new Ratelimit({
  redis: Redis.fromEnv(),
  limiter: Ratelimit.fixedWindow(5, "30 s"), // 5 requests per 30 sec window
});

const tokenBucket = new Ratelimit({
  redis: Redis.fromEnv(),
  limiter: Ratelimit.tokenBucket(10, "1 m", 20), // 10 refill/min, max 20 tokens
});

// Placeholder for an expensive operation
async function expensiveOperation() {
  return "Operation successful";
}
```

--------------------------------

### Get Substring of Redis Value (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/string/getrange

Retrieves a substring from a Redis string value using the GETRANGE command. Requires the Redis client instance, the key of the string, and the start and end indices for the substring. Returns the extracted substring.

```typescript
const substring = await redis.getrange("key", 2, 4);
```

--------------------------------

### Cloudflare Worker Code for Upstash Redis Integration (TypeScript and JavaScript)

Source: https://upstash.com/docs/redis/quickstarts/cloudflareworkers

Provides example Cloudflare Worker code for both TypeScript and JavaScript that connects to Upstash Redis using environment variables for credentials. It increments a 'counter' key in Redis and returns the updated count.

```typescript
import { Redis } from "@upstash/redis/cloudflare";

export interface Env {
  UPSTASH_REDIS_REST_URL: string;
  UPSTASH_REDIS_REST_TOKEN: string;
}

export default {
  async fetch(
    request: Request,
    env: Env,
    ctx: ExecutionContext
  ): Promise<Response> {
    const redis = Redis.fromEnv(env);
    const count = await redis.incr("counter");
    return new Response(JSON.stringify({ count }));
  },
};

```

```javascript
import { Redis } from "@upstash/redis/cloudflare";

export default {
  async fetch(request, env, ctx) {
    const redis = Redis.fromEnv(env);
    const count = await redis.incr("counter");
    return new Response(JSON.stringify({ count }));
  },
};

```

--------------------------------

### Get JSON Object Key Count with Upstash Redis (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/json/objlen

This example demonstrates how to use the JSON.OBJLEN command with Upstash Redis in TypeScript to find the number of keys in a JSON object. It requires the redis client and specifies the key and path of the JSON data.

```typescript
const lengths = await redis.json.objlen("key", "$.path");
```

--------------------------------

### Install Dependencies for FastAPI Session Management

Source: https://upstash.com/docs/redis/tutorials/python_session

Installs the necessary Python libraries for building a FastAPI application with Upstash Redis session management. This includes FastAPI itself, the Upstash Redis client, Uvicorn for running the server, and python-dotenv for managing environment variables.

```bash
pip install fastapi upstash-redis uvicorn python-dotenv
```

--------------------------------

### GET /websites/upstash-redis

Source: https://upstash.com/docs/redis/sdks/ts/commands/string/get

Retrieves the value associated with a specified key from the Upstash Redis instance. If the key does not exist, it returns null.

```APIDOC
## GET /websites/upstash-redis

### Description
Returns the value of the specified key or `null` if the key doesn't exist.

### Method
GET

### Endpoint
/websites/upstash-redis

### Parameters
#### Query Parameters
- **key** (string) - Required - The key to get the value for.

### Request Example
```ts
const value = await redis.get<MyType>("key");
```

### Response
#### Success Response (200)
- **value** (any) - The value stored at the key or `null` if the key doesn't exist.

#### Response Example
```json
{
  "value": "some_value"
}
```
```

--------------------------------

### Configure Upstash Redis Environment Variables

Source: https://upstash.com/docs/redis/quickstarts/nextjs-app-router

Sets the necessary environment variables for connecting to Upstash Redis. These variables, `UPSTASH_REDIS_REST_URL` and `UPSTASH_REDIS_REST_TOKEN`, are typically found in your Upstash dashboard and are crucial for initializing the Redis client.

```env
UPSTASH_REDIS_REST_URL=https://holy-kite-17499.upstash.io
UPSTASH_REDIS_REST_TOKEN=AURbAAIncDEyYjM4M...
```

--------------------------------

### Add Upstash Redis to requirements.txt

Source: https://upstash.com/docs/redis/quickstarts/vercel-python-runtime

Includes the `upstash-redis` package in the `requirements.txt` file, ensuring it is installed within the project's environment. This makes the Upstash Redis client library available for use.

```txt
Django==4.1.3
upstash-redis
```

--------------------------------

### Basic Redis Commands via REST

Source: https://context7.com/context7/upstash-redis/llms.txt

Execute standard Redis commands like SET, GET, MGET, HGET, and ZADD using simple HTTP GET and POST requests.

```APIDOC
## GET /<key>

### Description
Retrieves the value associated with a given key.

### Method
GET

### Endpoint
`https://<your-domain>.upstash.io/get/<key>`

### Parameters
#### Path Parameters
- **key** (string) - Required - The key to retrieve.

#### Query Parameters
None

#### Request Body
None

### Request Example
```bash
curl https://us1-merry-cat-32748.upstash.io/get/foo \
  -H "Authorization: Bearer <YOUR_TOKEN>"
```

### Response
#### Success Response (200)
- **result** (string) - The value of the key.

#### Response Example
```json
{
  "result": "bar"
}
```

---

## POST /set/<key>/<value>

### Description
Sets a key-value pair. Can also include expiration options like EX.

### Method
POST

### Endpoint
`https://<your-domain>.upstash.io/set/<key>/<value>`

### Parameters
#### Path Parameters
- **key** (string) - Required - The key to set.
- **value** (string) - Required - The value to associate with the key.

#### Query Parameters
- **EX** (integer) - Optional - Sets the specified expire time, in seconds.

#### Request Body
None (for basic key-value pairs)

### Request Example
```bash
# Set a key-value pair
curl https://us1-merry-cat-32748.upstash.io/set/foo/bar \
  -H "Authorization: Bearer <YOUR_TOKEN>"

# Set with expiration (100 seconds)
curl https://us1-merry-cat-32748.upstash.io/set/key/value/EX/100 \
  -H "Authorization: Bearer <YOUR_TOKEN>"
```

### Response
#### Success Response (200)
- **result** (string) - Indicates success, typically "OK".

#### Response Example
```json
{
  "result": "OK"
}
```

---

## GET /mget/<key1>/<key2>...

### Description
Retrieves the values for multiple keys.

### Method
GET

### Endpoint
`https://<your-domain>.upstash.io/mget/<key1>/<key2>/...`

### Parameters
#### Path Parameters
- **key1**, **key2**, ... (string) - Required - The keys to retrieve.

#### Query Parameters
None

#### Request Body
None

### Request Example
```bash
curl https://us1-merry-cat-32748.upstash.io/mget/key1/key2/key3 \
  -H "Authorization: Bearer <YOUR_TOKEN>"
```

### Response
#### Success Response (200)
- **result** (array) - An array of values corresponding to the requested keys.

#### Response Example
```json
{
  "result": ["value1", "value2", "value3"]
}
```

---

## GET /hget/<hash_key>/<field>

### Description
Retrieves the value of a field within a hash.

### Method
GET

### Endpoint
`https://<your-domain>.upstash.io/hget/<hash_key>/<field>`

### Parameters
#### Path Parameters
- **hash_key** (string) - Required - The key of the hash.
- **field** (string) - Required - The field within the hash.

#### Query Parameters
None

#### Request Body
None

### Request Example
```bash
curl https://us1-merry-cat-32748.upstash.io/hget/employee:23381/salary \
  -H "Authorization: Bearer <YOUR_TOKEN>"
```

### Response
#### Success Response (200)
- **result** (string) - The value of the specified field.

#### Response Example
```json
{
  "result": "<field_value>"
}
```

---

## POST /zadd/<key>/<score1>/<member1>/<score2>/<member2>...

### Description
Adds one or more members to a sorted set, or updates their score if they already exist.

### Method
POST

### Endpoint
`https://<your-domain>.upstash.io/zadd/<key>/<score1>/<member1>/<score2>/<member2>/...`

### Parameters
#### Path Parameters
- **key** (string) - Required - The key of the sorted set.
- **score1**, **score2**, ... (numeric) - Required - The scores of the members.
- **member1**, **member2**, ... (string) - Required - The members to add.

#### Query Parameters
None

#### Request Body
None

### Request Example
```bash
curl https://us1-merry-cat-32748.upstash.io/zadd/teams/100/team-x/90/team-y \
  -H "Authorization: Bearer <YOUR_TOKEN>"
```

### Response
#### Success Response (200)
- **result** (integer) - The number of elements added to the sorted set.

#### Response Example
```json
{
  "result": 2
}
```
```

--------------------------------

### Multi-Region Rate Limiter Setup

Source: https://upstash.com/docs/redis/sdks/ratelimit-ts/features

This code illustrates how to initialize a `MultiRegionRatelimit` client in TypeScript. It requires an array of `Redis` instances, each configured for a different region, and specifies the rate limiting algorithm (e.g., sliding window) and analytics settings. This setup ensures low latency for users by connecting to the closest Redis database.

```typescript
import { MultiRegionRatelimit } from "@upstash/ratelimit"; // for deno: see above
import { Redis } from "@upstash/redis";

// Create a new ratelimiter, that allows 10 requests per 10 seconds
const ratelimit = new MultiRegionRatelimit({
  redis: [
    new Redis({
      /* auth */
    }),
    new Redis({
      /* auth */
    }),
    new Redis({
      /* auth */
    }),
  ],
  limiter: MultiRegionRatelimit.slidingWindow(10, "10 s"),
  analytics: true,
});

// Use a constant string to limit all requests with a single ratelimit
// Or use a userID, apiKey or ip address for individual limits.
const identifier = "api";
const { success } = await ratelimit.limit(identifier);
```

--------------------------------

### Django URL Configuration for View

Source: https://upstash.com/docs/redis/quickstarts/django

Python code to map a URL pattern to the Django view function. This makes the view accessible via a specific URL in the web application.

```python
from django.urls import path
from myapp import views

urlpatterns = [
    path('', views.index),
]
```

--------------------------------

### Deno Redis Client Setup

Source: https://upstash.com/docs/redis/sdks/ts/deployment

Initializes the Upstash Redis client for Deno environments, including Deno Deploy and Netlify Edge. The client can be configured with explicit URL and token, or loaded directly from environment variables using `Redis.fromEnv()`.

```typescript
import { Redis } from "https://deno.land/x/upstash_redis/mod.ts"

const redis = new Redis({
  url: <UPSTASH_REDIS_REST_URL>,
  token: <UPSTASH_REDIS_REST_TOKEN>,
})

// or
const redis = Redis.fromEnv();
```

--------------------------------

### Run Nuxt Development Server and Test Endpoint

Source: https://upstash.com/docs/redis/tutorials/nuxtjs_with_redis

Commands to start the Nuxt development server and test the defined API endpoint. This includes instructions for running the application locally and making a curl request to the increment endpoint.

```bash
npm run dev
curl http://localhost:3000/api/increment
```

--------------------------------

### Initialize Upstash Redis Client from Environment (Python)

Source: https://upstash.com/docs/redis/sdks/py/gettingstarted

Shows how to initialize synchronous and asynchronous Upstash Redis clients by automatically loading credentials from environment variables. This is a convenient way to manage secrets.

```python
# for sync use
from upstash_redis import Redis
redis = Redis.from_env()

# for async use
from upstash_redis.asyncio import Redis
redis = Redis.from_env()
```

--------------------------------

### TypeScript Rate Limiting - Advanced Features

Source: https://context7.com/context7/upstash-redis/llms.txt

This TypeScript code demonstrates advanced rate limiting configurations with Upstash. It includes multi-region setups for low latency, defining different rate limits for user tiers, custom token consumption based on request size, and implementing a timeout fallback for Redis unavailability. Ensure dependencies are installed.

```typescript
import { Ratelimit } from "@upstash/ratelimit";
import { Redis } from "@upstash/redis";

// --- Multi-region configuration ---
// Replace with your actual URLs and Tokens
const US_URL = "YOUR_US_REDIS_URL";
const US_TOKEN = "YOUR_US_REDIS_TOKEN";
const EU_URL = "YOUR_EU_REDIS_URL";
const EU_TOKEN = "YOUR_EU_REDIS_TOKEN";
const ASIA_URL = "YOUR_ASIA_REDIS_URL";
const ASIA_TOKEN = "YOUR_ASIA_REDIS_TOKEN";

const ratelimitMultiRegion = new Ratelimit({
  redis: [
    new Redis({ url: US_URL, token: US_TOKEN }),
    new Redis({ url: EU_URL, token: EU_TOKEN }),
    new Redis({ url: ASIA_URL, token: ASIA_TOKEN }),
  ],
  limiter: Ratelimit.slidingWindow(100, "1 m"),
  analytics: true,
});

// --- Different limits for different user tiers ---
async function rateLimitByTier(userId: string, tier: string) {
  const limits = {
    free: new Ratelimit({
      redis: Redis.fromEnv(),
      limiter: Ratelimit.slidingWindow(10, "1 m"),
    }),
    pro: new Ratelimit({
      redis: Redis.fromEnv(),
      limiter: Ratelimit.slidingWindow(100, "1 m"),
    }),
    enterprise: new Ratelimit({
      redis: Redis.fromEnv(),
      limiter: Ratelimit.slidingWindow(1000, "1 m"),
    }),
  };

  const limiter = limits[tier] || limits.free;
  return await limiter.limit(userId);
}

// --- Custom token consumption based on request size ---
const ratelimitTokenBased = new Ratelimit({
  redis: Redis.fromEnv(),
  limiter: Ratelimit.tokenBucket(1000, "1 m", 2000), // 1000 refill/min, max 2000 tokens
});

interface File {
  size: number;
}

async function handleUpload(file: File, userId: string) {
  const tokens = Math.ceil(file.size / 1024); // 1 token per KB
  const { success, pending } = await ratelimitTokenBased.limit(userId, { rate: tokens });

  if (!success) {
    return { error: "Rate limit exceeded" };
  }

  // Wait for background tasks (analytics, multi-region sync)
  await pending;

  return { success: true };
}

// --- Timeout fallback for Redis unavailability ---
const ratelimitWithTimeout = new Ratelimit({
  redis: Redis.fromEnv(),
  limiter: Ratelimit.slidingWindow(10, "10 s"),
  timeout: 1000, // Allow request if Redis doesn't respond in 1s
  analytics: true,
});

// Example usage (assuming File interface and expensiveOperation are defined elsewhere)
// async function main() {
//   const userId = "user123";
//   const fileToUpload = { size: 5000 }; // 5KB file
//   const tier = "pro";

//   // Basic rate limiting check
//   const basicLimit = await ratelimit.limit(userId);
//   console.log("Basic limit success:", basicLimit.success);

//   // Tier-based rate limiting
//   const tierLimit = await rateLimitByTier(userId, tier);
//   console.log(`Tier '${tier}' limit success:`, tierLimit.success);

//   // Token-based upload rate limiting
//   const uploadResult = await handleUpload(fileToUpload, userId);
//   console.log("Upload result:", uploadResult);

//   // Rate limiting with timeout (simulate a slow Redis response)
//   // In a real scenario, you might mock Redis to simulate a timeout
//   const timeoutResult = await ratelimitWithTimeout.limit(userId);
//   console.log("Timeout fallback success:", timeoutResult.success);
// }

// main();

```

--------------------------------

### Retrieve Value by Key using Redis GET (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/string/get

This snippet demonstrates how to use the Upstash Redis GET command to retrieve a value associated with a specific key. It handles cases where the key might not exist and shows how to use TypeScript generics for type safety on the retrieved value. Ensure the 'redis' client is initialized before use.

```typescript
type MyType = {
    a: number;
    b: string;
}
const value = await redis.get<MyType>("key");
if (!value) {
    // key doesn't exist
} else {
    // value is of type MyType
}
```

--------------------------------

### Get JSON String Length with Upstash Redis (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/json/strlen

This example demonstrates how to use the JSON.STRLEN command with Upstash Redis in TypeScript. It requires the 'redis' client library. The function takes a key and a JSON path as input and returns the length of the JSON string found at that path.

```typescript
await redis.json.strlen("key", "$.path.to.str", "a");
```

--------------------------------

### Retrieve Stream Entries with XRANGE in TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/stream/xrange

This TypeScript example demonstrates how to use the Upstash Redis XRANGE command to fetch entries from a stream. It takes the stream key, start ID ('-'), end ID ('+'), and optionally a count as arguments. The output is a console log of the retrieved stream entries, which are structured as an object keyed by stream ID.

```typescript
const entries = redis.xrange(key, "-", "+");
console.log(entries)
// {
//   "1548149259438-0": {
//     "field1": "value1",
//     "field2": "value2"
//   },
//   "1548149259438-1": {
//     "field1": "value3",
//     "field2": "value4"
//   }
// }
```

--------------------------------

### Python Redis Pipelines, Transactions, and Chaining

Source: https://context7.com/context7/upstash-redis/llms.txt

This Python code demonstrates how to batch multiple Redis commands using pipelines for efficiency, execute commands atomically using transactions, and chain commands for sequential execution. It utilizes the `redis` library to interact with an Upstash Redis instance. Ensure the `redis` library is installed (`pip install redis`).

```python
redis = Redis.from_env()
pipeline = redis.pipeline()

pipeline.set("key1", "value1")
pipeline.incr("counter")
pipeline.get("counter")
pipeline.zadd("scores", {"score": 100, "member": "player1"})

results = pipeline.exec()
print(results)  # [True, 1, "1", 1]

# Transactions - atomic execution
transaction = redis.multi()

transaction.set("balance:alice", 1000)
transaction.decrby("balance:alice", 100)
transaction.incrby("balance:bob", 100)

results = transaction.exec()
print(results)  # [True, 900, 100]

# Chain commands
pipeline = redis.pipeline()
result = pipeline.set("a", 1).incr("a").get("a").exec()
print(result)  # [True, 2, "2"]
```

--------------------------------

### Initialize Project and Add Sidekiq (Bash)

Source: https://upstash.com/docs/redis/integrations/sidekiq

This snippet demonstrates the initial steps to set up a Ruby project and add the Sidekiq gem. It assumes you are in a project directory and uses Bundler for dependency management.

```bash
bundle init 
bundle add sidekiq
```

--------------------------------

### Get Reverse Rank of Member in Sorted Set (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/zset/zrevrank

This snippet demonstrates how to use the ZREVRANK command in Python with Upstash Redis. It adds members to a sorted set and then retrieves the reverse rank of a specific member. Ensure you have the Upstash Redis client library installed.

```python
redis.zadd("myset", {"a": 1, "b": 2, "c": 3})

assert redis.zrevrank("myset", "a") == 2
```

--------------------------------

### Get Member Score in Redis Sorted Set (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/zset/zscore

This TypeScript example demonstrates how to add members with scores to a Redis sorted set using ZADD and then retrieve the score of a specific member using ZSCORE. It assumes an existing Redis client instance named 'redis'.

```typescript
await redis.zadd("key", 
    { score: 1, member: "m1" },
    { score: 2, member: "m2" },
    { score: 3, member: "m3" },
    { score: 4, member: "m4" },
)

const score = await redis.zscore("key", "m2")
console.log(score) // 2
```

--------------------------------

### Configure and Use BullMQ with Upstash Redis in JavaScript

Source: https://upstash.com/docs/redis/integrations/bullmq

Demonstrates how to initialize a BullMQ queue with Upstash Redis connection details and add jobs to the queue. It requires the 'bullmq' and 'upstash-redis' packages to be installed. The function `addJobs` adds two sample jobs to the 'foo' queue.

```javascript
import { Queue } from 'bullmq';

const myQueue = new Queue('foo', { connection: {
        host: "UPSTASH_REDIS_ENDPOINT",
        port: 6379,
        password: "UPSTASH_REDIS_PASSWORD",
        tls: {}
    }});

async function addJobs() {
    await myQueue.add('myJobName', { foo: 'bar' });
    await myQueue.add('myJobName', { qux: 'baz' });
}

await addJobs();
```

--------------------------------

### Dockerfile for Node.js Express App

Source: https://upstash.com/docs/redis/tutorials/cloud_run_sessions

A Dockerfile to containerize a Node.js Express application. It uses a lightweight Node.js 12 image, sets the working directory, copies package manifests, installs dependencies using `npm install`, and then copies the rest of the application code into the container.

```dockerfile
# Use the official lightweight Node.js 12 image.
# https://hub.docker.com/_/node
FROM node:12-slim

# Create and change to the app directory.
WORKDIR /usr/src/app

# Copy application dependency manifests to the container image.
# A wildcard is used to ensure both package.json AND package-lock.json are copied.
# Copying this separately prevents re-running npm install on every code change.
COPY package*.json ./

# Install dependencies.
RUN npm install

# Copy local code to the container image.
COPY . ./
```

--------------------------------

### Python ZREMRANGEBYRANK Example - Upstash Redis

Source: https://upstash.com/docs/redis/sdks/py/commands/zset/zremrangebyrank

This Python code snippet demonstrates how to use the ZREMRANGEBYRANK command to remove elements from a sorted set in Upstash Redis. It takes the sorted set key, minimum rank, and maximum rank as input and returns the count of removed elements. Ensure the 'redis' library is installed and configured.

```python
redis.zremrangebyrank("key", 4, 20)
```

--------------------------------

### Upstash Redis SPOP Command Example (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/set/spop

Demonstrates how to use the SPOP command to remove and return a random member from a set. It first adds members to the set and then calls spop. This example is for a single member.

```typescript
await redis.sadd("set", "a", "b", "c"); 
const popped = await redis.spop("set");
console.log(popped); // "a"
```

--------------------------------

### Fastly Publish and Configure Upstash Backend

Source: https://upstash.com/docs/redis/quickstarts/fastlycompute

This sequence of commands publishes a Fastly Compute package and configures an Upstash Redis instance as a backend. It includes prompts for creating a new service, setting the domain, and defining the Upstash backend with its port and name.

```shell
> fastly compute publish
✓ Initializing...
✓ Verifying package manifest...
✓ Verifying local javascript toolchain...
✓ Building package using javascript toolchain...
✓ Creating package archive...

SUCCESS: Built package 'fastly-upstash' (pkg/fastly-upstash.tar.gz)


There is no Fastly service associated with this package. To connect to an existing service
add the Service ID to the fastly.toml file, otherwise follow the prompts to create a
service now.

Press ^C at any time to quit.

Create new service: [y/N] y

✓ Initializing...
✓ Creating service...

Domain: [supposedly-included-corgi.edgecompute.app]

Backend (hostname or IP address, or leave blank to stop adding backends): global-concise-scorpion-30984.upstash.io
Backend port number: [80] 443
Backend name: [backend_1] upstash

Backend (hostname or IP address, or leave blank to stop adding backends):

✓ Creating domain 'supposedly-smart-corgi.edgecompute.app'...
✓ Creating backend 'upstash' (host: global-concise-scorpion-30984.upstash.io, port: 443)...
✓ Uploading package...
✓ Activating version...
```

--------------------------------

### Get JSON Object Key Count using Python

Source: https://upstash.com/docs/redis/sdks/py/commands/json/objlen

This Python snippet demonstrates how to use the Upstash Redis client to retrieve the number of keys in a JSON object. It requires the 'redis' library to be installed and configured with your Upstash Redis connection details. The function takes the key and the path to the JSON object as input.

```python
lengths = redis.json.objlen("key", "$.path")
```

--------------------------------

### Execute Redis KEYS Command (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/generic/keys

This Python code snippet demonstrates how to use the Upstash Redis client to execute the KEYS command. It shows examples for matching keys with a specific prefix and for matching all keys. Note the warning against using this in production.

```python
redis.keys("prefix*")
```

```python
redis.keys("*")
```

--------------------------------

### Get Hash Field Expiration Time (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/hash/hpexpiretime

This TypeScript example demonstrates how to use the `hpexpiretime` command with Upstash Redis. It first sets a field in a hash, sets an expiration for that field, and then retrieves the expiration time. The result is logged to the console. Assumes `redis` is an initialized Upstash Redis client.

```typescript
await redis.hset("my-key", "my-field", "my-value");
await redis.hpexpireat("my-key", "my-field", Date.now() + 1000);
const expireTime = await redis.hpexpiretime("my-key", "my-field");

console.log(expireTime); // e.g., 1697059200000
```

--------------------------------

### PSUBSCRIBE to Channels with Patterns in TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/pubsub/psubscribe

Subscribe to channels using wildcard patterns with the PSUBSCRIBE command. This example demonstrates how to set up a subscription, handle incoming messages, and publish messages to test the pattern matching.

```typescript
const subscription = redis.psubscribe(["user:*"]);

const messages = [];
subscription.on("pmessage", (data) => {
  messages.push(data.message);
});

await redis.publish("user:123", "user:123 message"); // receives
await redis.publish("user:456", "user:456 message"); // receives
await redis.publish("other:789", "other:789 message"); // doesn't receive

console.log(messages[0]) // user:123 message
console.log(messages[1]) // user:456 message
console.log(messages[2]) // undefined
```

--------------------------------

### Initialize Git Repository and Push to GitHub

Source: https://upstash.com/docs/redis/quickstarts/koyeb

This sequence of bash commands initializes a Git repository, adds project files (excluding node_modules), commits them with a message, sets the remote origin to a GitHub repository, and pushes the initial commit. This is a standard workflow for version control and deployment.

```bash
git init
echo 'node_modules' >> .gitignore
git add .
git commit -m "Initial commit"
git remote add origin git@github.com:<YOUR_GITHUB_USERNAME>/<YOUR_REPOSITORY_NAME>.git
git push -u origin main
```

--------------------------------

### Install Drizzle ORM Cache Package

Source: https://upstash.com/docs/redis/integrations/drizzle

Installs the necessary Drizzle ORM package with caching capabilities using npm. This is the first step to enable caching features.

```bash
npm install drizzle-orm@cache
```

--------------------------------

### Upstash Redis REST API - Basic Commands (Bash)

Source: https://context7.com/context7/upstash-redis/llms.txt

Execute fundamental Redis commands like SET, GET, MGET, HGET, and ZADD using the Upstash Redis REST API. These commands are sent as HTTP GET or POST requests to the Upstash endpoint.

```bash
# Set a key-value pair
curl https://us1-merry-cat-32748.upstash.io/set/foo/bar \
  -H "Authorization: Bearer 2553feg6a2d9842h2a0gcdb5f8efe9934"

# Response: {"result":"OK"}

# Get a value
curl https://us1-merry-cat-32748.upstash.io/get/foo \
  -H "Authorization: Bearer 2553feg6a2d9842h2a0gcdb5f8efe9934"

# Response: {"result":"bar"}

# Set with expiration (100 seconds)
curl https://us1-merry-cat-32748.upstash.io/set/key/value/EX/100 \
  -H "Authorization: Bearer 2553feg6a2d9842h2a0gcdb5f8efe9934"

# Get multiple keys
curl https://us1-merry-cat-32748.upstash.io/mget/key1/key2/key3 \
  -H "Authorization: Bearer 2553feg6a2d9842h2a0gcdb5f8efe9934"

# Response: {"result":["value1","value2","value3"]}

# Hash operations
curl https://us1-merry-cat-32748.upstash.io/hget/employee:23381/salary \
  -H "Authorization: Bearer 2553feg6a2d9842h2a0gcdb5f8efe9934"

# Sorted set operations
curl https://us1-merry-cat-32748.upstash.io/zadd/teams/100/team-x/90/team-y \
  -H "Authorization: Bearer 2553feg6a2d9842h2a0gcdb5f8efe9934"
```

--------------------------------

### Deploy AWS SAM Application

Source: https://upstash.com/docs/redis/tutorials/using_aws_sam

This command deploys the AWS SAM application to AWS. The `--guided` flag initiates an interactive deployment process, prompting the user for necessary configuration details, including environment variables for Upstash Redis.

```shell
sam deploy --guided
```

--------------------------------

### TypeScript: Ratelimit blockUntilReady Usage Example

Source: https://upstash.com/docs/redis/sdks/ratelimit-ts/methods

An example demonstrating how to use the `blockUntilReady` method to wait for a request to be processed within a specified timeout. It shows how to handle cases where the request cannot be processed within the given time.

```ts
// Create a new ratelimiter, that allows 10 requests per 10 seconds
const ratelimit = new Ratelimit({
  redis: Redis.fromEnv(),
  limiter: Ratelimit.slidingWindow(10, "10 s"),
  analytics: true,
});

// `blockUntilReady` returns a promise that resolves as soon as the request is allowed to be processed, or after 30 seconds
const { success } = await ratelimit.blockUntilReady("id", 30000);

if (!success) {
  return "Unable to process, even after 30 seconds";
}
doExpensiveCalculation();
return "Here you go!";
```

--------------------------------

### Connect and Use Redis CLI with Upstash Redis

Source: https://upstash.com/docs/redis/index

Demonstrates how to connect to an Upstash Redis database using the redis-cli and execute basic commands like SET, GET, and INCR. This requires the database endpoint, port, and password. It shows the typical output for each command.

```shell
> redis-cli --tls -a PASSWORD -h ENDPOINT -p PORT
ENDPOINT:PORT> set counter 0
OK
ENDPOINT:PORT> get counter
"0"
ENDPOINT:PORT> incr counter
(int) 1
ENDPOINT:PORT> incr counter
(int) 2
```

--------------------------------

### Create and Activate Conda Environment

Source: https://upstash.com/docs/redis/quickstarts/vercel-python-runtime

Sets up a Conda environment named `vercel-django` with Python 3.12 and installs project dependencies from `requirements.txt`. This ensures a consistent environment for deployment.

```shell
conda create --name vercel-django python=3.12
conda activate vercel-django
pip install -r requirements.txt
```

--------------------------------

### Serverless Framework Configuration for Histogram API

Source: https://upstash.com/docs/redis/tutorials/histogram

Defines the serverless service configuration in `serverless.yml`. It specifies the AWS provider, Node.js runtime, and environment variables, including the crucial `REDIS_URL`. Two HTTP API functions, 'record' (POST) and 'get' (GET), are configured with their respective handlers and paths.

```yaml
service: histogram-api
frameworkVersion: "2"

provider:
  name: aws
  runtime: nodejs12.x
  lambdaHashingVersion: 20201221
  environment:
    REDIS_URL: REPLACE_YOUR_URL_HERE

functions:
  record:
    handler: handler.record
    events:
      - httpApi:
          path: /record
          method: post
          cors: true
  get:
    handler: handler.get
    events:
      - httpApi:
          path: /get
          method: get
          cors: true
```

--------------------------------

### Install Upstash Redis Dependency (Python)

Source: https://upstash.com/docs/redis/tutorials/using_aws_sam

This file lists the Python dependencies for the Lambda function. It includes the 'upstash-redis' package, which is necessary for interacting with Upstash Redis.

```txt
requests
upstash-redis
```

--------------------------------

### Flask and Socket.IO Setup with Redis

Source: https://upstash.com/docs/redis/tutorials/python_realtime_chat

Initializes a Flask application, configures Socket.IO to use Upstash Redis for message brokering, and defines WebSocket event handlers for connecting, disconnecting, and message broadcasting. It sets up a route to serve the chat interface.

```python
from flask import Flask, render_template
from flask_socketio import SocketIO
import os

app = Flask(__name__)
app.config['SECRET_KEY'] = os.environ.get('SECRET_KEY', 'a_default_secret_key')

# Configure Redis URL with TLS for secure communication
redis_url = os.environ.get('REDIS_URL')

# Initialize SocketIO with Flask app and Redis configuration
socketio = SocketIO(app, message_queue=redis_url, 
                    cors_allowed_origins="*",
                    logger=True, engineio_logger=True)

@socketio.on('connect')
def handle_connect():
    print('Client connected')

@socketio.on('disconnect')
def handle_disconnect():
    print('Client disconnected')

@socketio.on('message')
def handle_message(data):
    # Broadcast message to all clients except the sender
    sender_sid = request.sid
    socketio.emit('message', data, include_self=False)
    print(f"Received message: {data}")

@app.route('/')
def chat():
    return render_template('chat.html')

if __name__ == '__main__':
    socketio.run(app, debug=True, host='0.0.0.0', port=int(os.environ.get('PORT', 5000)))

```

--------------------------------

### Rate Limiter Response Metadata (Python)

Source: https://upstash.com/docs/redis/sdks/ratelimit-py/gettingstarted

Defines the `Response` dataclass for the Upstash rate limiter, detailing the metadata returned with each limiting operation. This includes whether the request was allowed, the limit, remaining requests, and the reset time.

```python
@dataclasses.dataclass
class Response:
    allowed: bool
    """
    Whether the request may pass(`True`) or exceeded the limit(`False`)
    """

    limit: int
    """
    Maximum number of requests allowed within a window.
    """

    remaining: int
    """
    How many requests the user has left within the current window.
    """

    reset: float
    """
    Unix timestamp in seconds when the limits are reset
    """
```

--------------------------------

### Connect to Upstash Redis using JavaScript SDK

Source: https://upstash.com/docs/redis/quickstarts/koyeb

Demonstrates how to initialize the Upstash Redis client with URL and token. It then sets a key-value pair. Ensure to replace placeholder credentials with your actual Upstash database URL and token. Sensitive data should ideally be managed through environment variables rather than hardcoded.

```javascript
import { Redis } from "@upstash/redis";

const redis = new Redis({
  url: "<YOUR_UPSTASH_REDIS_REST_URL>",
  token: "<YOUR_UPSTASH_REDIS_REST_TOKEN>",
});

const data = await redis.set("foo", "bar");
```

--------------------------------

### Perform BITOP AND Operation with Upstash Redis Client

Source: https://upstash.com/docs/redis/sdks/ts/commands/bitmap/bitop

This example demonstrates how to use the Upstash Redis client to perform a bitwise AND operation between two source keys and store the result in a destination key. It requires the Redis client to be initialized and connected.

```typescript
await redis.bitop("AND", "destKey", "sourceKey1", "sourceKey2");
```

--------------------------------

### Get Koyeb App Details

Source: https://upstash.com/docs/redis/quickstarts/koyeb

Fetches the details of a deployed Koyeb application, including its ID, name, assigned domains, and creation timestamp. This is useful for retrieving the application's public URL.

```bash
koyeb app get example-koyeb-upstash
```

--------------------------------

### Redis BITCOUNT Command with Python Example

Source: https://upstash.com/docs/redis/sdks/py/commands/bitmap/bitcount

Demonstrates how to use the BITCOUNT command in Redis with Python. It shows setting bits and then counting them with and without specifying a range. Requires the redis-py library.

```python
redis.setbit("mykey", 7, 1)
redis.setbit("mykey", 8, 1)
redis.setbit("mykey", 9, 1)

# With range
assert redis.bitcount("mykey", 0, 10) == 3

# Without range
assert redis.bitcount("mykey") == 3
```

--------------------------------

### Connect and use upstash-redis client (TypeScript)

Source: https://upstash.com/docs/redis/howto/connectwithupstashredis

Demonstrates how to connect to Upstash Redis using explicit URL and token. It shows a basic GET operation and error handling. This method requires manual configuration of credentials.

```typescript
import { Redis } from "@upstash/redis";

const redis = new Redis({
  url: "UPSTASH_REDIS_REST_URL",
  token: "UPSTASH_REDIS_REST_TOKEN",
});

(async () => {
  try {
    const data = await redis.get("key");
    console.log(data);
  } catch (error) {
    console.error(error);
  }
})();
```

--------------------------------

### Node.js/Browser Redis Client Setup

Source: https://upstash.com/docs/redis/sdks/ts/deployment

Initializes the Upstash Redis client for Node.js and browser environments. It can be configured with explicit URL and token, or by loading directly from environment variables. Ensure `fetch` is available, either natively or via a polyfill.

```typescript
import { Redis } from "@upstash/redis"

const redis = new Redis({
  url: <UPSTASH_REDIS_REST_URL>,
  token: <UPSTASH_REDIS_REST_TOKEN>,
})

// or load directly from env
const redis = Redis.fromEnv()
```

```typescript
import { Redis } from "@upstash/redis/with-fetch";
```

--------------------------------

### Redis LPUSHX Command Example (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/list/lpushx

Demonstrates the usage of the LPUSHX command in TypeScript. It shows pushing an element to an existing list and the case where the list does not exist. The command requires the key and the element(s) to push. It returns the new length of the list or 0.

```typescript
await redis.lpush("key", "a", "b", "c"); 
const length = await redis.lpushx("key", "d"); 
console.log(length); // 4
```

```typescript
const length = await redis.lpushx("key", "a"); 
console.log(length); // 0
```

--------------------------------

### Python RENAMENX Example - Upstash Redis

Source: https://upstash.com/docs/redis/sdks/py/commands/generic/renamenx

Demonstrates the usage of the RENAMENX command in Python with Upstash Redis. It shows how to rename a key if the destination does not exist and verifies the outcome. This function requires a Redis client instance.

```python
redis.set("key1", "Hello")
redis.set("key2", "World")

# Rename failed because "key2" already exists.
assert redis.renamenx("key1", "key2") == False

assert redis.renamenx("key1", "key3") == True

assert redis.get("key1") is None
assert redis.get("key2") == "World"
assert redis.get("key3") == "Hello"
```

--------------------------------

### Redis SET with GET Option in Python

Source: https://upstash.com/docs/redis/sdks/py/commands/string/set

Illustrates using the GET option with the SET command to retrieve the previous value associated with the key before it was updated. This is useful for scenarios where you need to know the old state.

```python
# Get the old value stored at the key.
assert redis.set("key", "new-value", get=True) == "old-value"
```

--------------------------------

### RPUSH Command Example in Python

Source: https://upstash.com/docs/redis/sdks/py/commands/list/rpush

Demonstrates how to use the RPUSH command to add elements to the end of a list in Upstash Redis. It shows pushing multiple elements and then verifying the list content.

```python
assert redis.rpush("mylist", "one", "two", "three") == 3

assert lrange("mylist", 0, -1) == ["one", "two", "three"]
```

--------------------------------

### Create Cloudflare Worker Project with npm, yarn, or pnpm

Source: https://upstash.com/docs/redis/quickstarts/cloudflareworkers

Initializes a new Cloudflare Workers project named 'upstash-redis-worker' using different package managers. This sets up the basic project structure and dependencies for a Cloudflare Worker.

```shell
npm create cloudflare@latest -- upstash-redis-worker
```

```shell
yarn create cloudflare upstash-redis-worker
```

```shell
pnpm create cloudflare upstash-redis-worker
```

--------------------------------

### Create React App

Source: https://upstash.com/docs/redis/tutorials/notification

Command to create a new React application. This initializes a project structure suitable for frontend development.

```shell
npx create-react-app serverless-notification-api
```

--------------------------------

### Basic Redis SET in Python

Source: https://upstash.com/docs/redis/sdks/py/commands/string/set

Sets a key to hold a string value and verifies it using the GET command. This is the most basic usage of the SET command.

```python
assert redis.set("key", "value") == True

assert redis.get("key") == "value"
```

--------------------------------

### Map Redis Commands to REST API URL Structure (Examples)

Source: https://upstash.com/docs/redis/features/restapi

Illustrates how various Redis commands map to the REST API URL structure. Commands and their arguments are appended to the REST URL, separated by slashes.

```shell
SET foo bar -> REST_URL/set/foo/bar
SET foo bar EX 100 -> REST_URL/set/foo/bar/EX/100
GET foo -> REST_URL/get/foo
MGET foo1 foo2 foo3 -> REST_URL/mget/foo1/foo2/foo3
HGET employee:23381 salary -> REST_URL/hget/employee:23381/salary
ZADD teams 100 team-x 90 team-y -> REST_URL/zadd/teams/100/team-x/90/team-y
```

--------------------------------

### Install Upstash Redis SDK for Node.js

Source: https://upstash.com/docs/redis/tutorials/cloudflare_workers_with_redis

Installs the official Upstash Redis client library for Node.js using npm. This package enables your Cloudflare Worker to interact with your Upstash Redis database via its REST API.

```shell
cd greetings-cloudflare
npm install @upstash/redis
```

--------------------------------

### Add Redix Dependency to Mix Project (Elixir)

Source: https://upstash.com/docs/redis/quickstarts/elixir

Updates the 'mix.exs' file to include the 'redix' and 'castore' dependencies, essential for connecting to an Upstash Redis instance from an Elixir Phoenix application. After adding these, 'mix deps.get' must be run to install them.

```elixir
defp deps do
  [
    {:redix, "~> 1.1"},
    {:castore, ">= 0.0.0"}
  ]
end
```

--------------------------------

### RPUSHX Example in TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/list/rpushx

Demonstrates using the RPUSHX command to add an element to an existing list in TypeScript. It shows how to push 'd' to 'key' after an initial LPUSH, and logs the resulting list length. It also shows the behavior when the list does not exist, resulting in a length of 0.

```typescript
await redis.lpush("key", "a", "b", "c"); 
const length = await redis.rpushx("key", "d"); 
console.log(length); // 4

const length2 = await redis.rpushx("key_non_existent", "a"); 
console.log(length2); // 0
```

--------------------------------

### Connect and use upstash-redis client from environment variables (TypeScript)

Source: https://upstash.com/docs/redis/howto/connectwithupstashredis

Shows how to initialize the upstash-redis client by automatically loading credentials from environment variables. This simplifies configuration in serverless or deployment environments.

```typescript
import { Redis } from "@upstash/redis";

const redis = Redis.fromEnv()(async () => {
  try {
    const data = await redis.get("key");
    console.log(data);
  } catch (error) {
    console.error(error);
  }
})();
```

--------------------------------

### Get Key Type with Upstash Redis (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/generic/type

This Python code snippet demonstrates how to use the Upstash Redis client to get the data type of a key. It covers setting different data types and then verifying their types using the `redis.type()` method. It also shows the expected output for a non-existent key.

```python
redis.set("key1", "Hello")

assert redis.type("key1") == "string"

redis.lpush("key2", "Hello")

assert redis.type("key2") == "list"

assert redis.type("non-existent-key") == "none"
```

--------------------------------

### Example Serverless Function Output

Source: https://upstash.com/docs/redis/tutorials/auto_complete_with_serverless_redis

This JSON output represents the expected response from the 'query' serverless function when invoked. It includes the status code, headers, and a JSON string body containing the query term and a list of results.

```json
{
  "statusCode": 200,
  "headers": {
    "Access-Control-Allow-Origin": "*",
    "Access-Control-Allow-Credentials": true
  },
  "body": "{\"message\":\"Query:ca\",\"result\":[\"CAMBODIA\",\"CAMEROON\",\"CANADA\",\"CAPE VERDE\",\"CAYMAN ISLANDS\"]}"
}
```

--------------------------------

### Interact with Redis using Laravel Facade

Source: https://upstash.com/docs/redis/quickstarts/laravel

Demonstrates basic Redis operations (set and get) using the Redis Facade in Laravel. This allows direct interaction with the Redis database for storing and retrieving values.

```php
use Illuminate\Support\Facades\Redis;

// Storing a value in Redis
Redis::set('key', 'value');

// Retrieving a value from Redis
$value = Redis::get('key');
```

--------------------------------

### Phoenix HTML Template for Home Page

Source: https://upstash.com/docs/redis/quickstarts/elixir

This HEEX template defines the structure of the home page in a Phoenix application. It includes a form for user input (location) and displays weather information or connection status messages. It relies on `@flash`, `@text`, `@weather`, and `@location` assigns.

```html
<.flash_group flash={@flash} />
<div class="container mx-auto px-4">
  <h1 class="text-3xl font-bold mb-4">Redix Demo</h1>

  <form action="/" method="get" class="w-full flex items-center mb-4">
    <input type="text" name="text" placeholder="Location" class="flex-1 px-4 py-2 border border-gray-300 rounded-lg shadow-sm focus:outline-none focus:border-blue-500">
    <button type="submit" class="ml-4 px-4 py-2 bg-blue-500 text-white rounded-lg hover:bg-blue-600">Submit</button>
  </form>

  <%= if @text do %>
    <%= @text %>
  <% end %>

  <%= if @weather do %>
    <div class=" text-lg bg-gray-100 rounded-lg p-4">

      <%= if @location do %>
        <strong>
          Location:
        </strong>
        <%= @location %>
      <% end %>

      <p>
        <strong>
          Weather:
        </strong>
        <%= @weather %> °C
      </p>

    </div>
  <% end %>
</div>
```

--------------------------------

### Initialize Redix Client in Application Children (Elixir)

Source: https://upstash.com/docs/redis/quickstarts/elixir

Adds a configured Redix client instance to the list of supervised children in the 'application.ex' file. It utilizes the extracted host, port, and password, and includes 'socket_opts: [:inet6]' for Fly.io deployments, with a note to omit this for local testing.

```elixir
children = [
  # ...
  {
    Redix,
    name: :redix,
    host: host,
    port: port,
    password: password,
    socket_opts: [:inet6]
  }
]
```

--------------------------------

### Python SRANDMEMBER Example

Source: https://upstash.com/docs/redis/sdks/py/commands/set/srandmember

Demonstrates how to use the SRANDMEMBER command in Python with Upstash Redis. It shows adding members to a set and then retrieving a single random member or multiple random members.

```python
redis.sadd("myset", "one", "two", "three")

assert redis.srandmember("myset") in {"one", "two", "three"}
```

```python
redis.sadd("myset", "one", "two", "three")

assert redis.srandmember("myset", 2) in {"one", "two", "three"}
```

--------------------------------

### Django View to Increment Redis Counter

Source: https://upstash.com/docs/redis/quickstarts/django

Python code for a Django view that connects to Upstash Redis, increments a 'counter' key, and returns the current count in an HTTP response.

```python
from django.http import HttpResponse
from upstash_redis import Redis

redis = Redis.from_env()

def index(request):
    count = redis.incr('counter')
    return HttpResponse(f'Page visited {count} times.')
```

--------------------------------

### Flask Application with Upstash Redis Counter

Source: https://upstash.com/docs/redis/quickstarts/flask

A Python Flask application that connects to Upstash Redis using environment variables and increments a 'counter' key on each request to the root route. The current count is then displayed.

```python
from flask import Flask
from upstash_redis import Redis

app = Flask(__name__)

redis = Redis.from_env()

@app.route('/')
def index():
    count = redis.incr('counter')
    return f'Page visited {count} times.'

if __name__ == '__main__':
    app.run(debug=True)
```

--------------------------------

### Run the Python URL Shortener Application

Source: https://upstash.com/docs/redis/tutorials/python_url_shortener

Executes the Python script for the URL shortener. This command runs the `url_shortener.py` file, initiating the process of shortening a URL and interacting with Redis. The output will show the generated short URL and the retrieved original URL, or an expiration message.

```shell
python url_shortener.py
```

--------------------------------

### Test API Endpoints with cURL (Shell)

Source: https://upstash.com/docs/redis/tutorials/laravel_caching

Provides example cURL commands to interact with the Todo API, demonstrating how to fetch all todos, a specific todo, create, update, and delete todos. These commands are useful for testing the caching mechanisms implemented in the `TodoController`.

```shell
# Get all todos
curl http://todo-cache.test/api/todos

# Get a specific todo
curl http://todo-cache.test/api/todos/1

# Create a new todo
curl -X POST http://todo-cache.test/api/todos \
  -H "Content-Type: application/json" \
  -d '{"title":"New Todo"}'

# Update a todo
curl -X PUT http://todo-cache.test/api/todos/1 \
  -H "Content-Type: application/json" \
  -d '{"title":"Updated Todo"}'

# Delete a todo
curl -X DELETE http://todo-cache.test/api/todos/1
```

--------------------------------

### Python Redis ZINTER Intersection with Weights

Source: https://upstash.com/docs/redis/sdks/py/commands/zset/zinter

Illustrates using weights with the ZINTER command in Python for weighted intersections. This example applies specific weights to two sets before calculating the intersection and summing the scores.

```python
redis.zadd("key1", {"a": 1})

redis.zadd("key2", {"a": 1})

result = redis.zinter(["key1", "key2"],
                        withscores=True,
                        aggregate="SUM",
                        weights=[2, 3])

assert result == [("a", 5)]
```

--------------------------------

### Cloudflare Worker: Leaderboard API Implementation (JavaScript)

Source: https://upstash.com/docs/redis/tutorials/edge_leaderboard

This JavaScript code defines the Cloudflare Worker logic for a leaderboard API. It handles GET requests to fetch the leaderboard and POST requests to add scores, interacting with Upstash Redis. It also includes edge caching configuration for GET requests.

```javascript
addEventListener("fetch", (event) => {
  event.respondWith(handleRequest(event.request));
});

async function handleRequest(request) {
  if (request.method === "GET") {
    return getLeaderboard();
  } else if (request.method === "POST") {
    return addScore(request);
  } else {
    return new Response("Invalid Request!");
  }
}

async function getLeaderboard() {
  let url =
    "https://us1-full-bug-31874.upstash.io/zrevrange/scores/0/1000/WITHSCORES/?_token=" +
    TOKEN;
  let res = await fetch(new Request(url), {
    cf: {
      cacheTtl: 10,
      cacheEverything: true,
      cacheKey: url,
    },
  });
  return res;
}

async function addScore(request) {
  const { searchParams } = new URL(request.url);
  let player = searchParams.get("player");
  let score = searchParams.get("score");
  let url =
    "https://us1-full-bug-31874.upstash.io/zadd/scores/" +
    score +
    "/" +
    player +
    "?_token=" +
    TOKEN;
  let res = await fetch(url);
  return new Response(await res.text());
}
```

--------------------------------

### Scan a Set using SSCAN in TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/set/sscan

Demonstrates how to add members to a set and then scan them using the SSCAN command with a match pattern. The example shows how to use the returned cursor and members, and it assumes the `redis` client is already initialized.

```typescript
await redis.sadd("key", "a", "ab","b", "c");
const [newCursor, fields] = await redis.sscan("key", 0, { match: "a*"});
console.log(newCursor); // likely `0` since this is a very small set
console.log(fields); // ["a", "ab"]
```

--------------------------------

### Run FastAPI Application with Uvicorn

Source: https://upstash.com/docs/redis/tutorials/python_fastapi_caching

Starts the FastAPI application using the Uvicorn ASGI server. The `--reload` flag enables hot-reloading, which restarts the server whenever code changes are detected.

```shell
uvicorn main:app --reload
```

--------------------------------

### Run Node.js Application Locally (Shell)

Source: https://upstash.com/docs/redis/quickstarts/fly

This command starts your Node.js application. Ensure the Fly.io Redis tunnel is active when running this command locally to allow your application to connect to Redis via the tunnel.

```shell
npm start
```

--------------------------------

### Upstash Redis ZADD Simple Example

Source: https://upstash.com/docs/redis/sdks/ts/commands/zset/zadd

Adds members with specified scores to a sorted set. If a member already exists, its score is updated. This is the basic usage without any special options.

```typescript
await redis.zadd(
    "key", 
    { score: 2, member: "member" }, 
    { score: 3, member: "member2"},
);
```

--------------------------------

### BITPOS

Source: https://upstash.com/docs/redis/sdks/ts/commands/bitmap/bitpos

Finds the position of the first set or clear bit in a Redis string key. Supports optional start and end indices for the search range.

```APIDOC
## BITPOS

### Description
Finds the position of the first set or clear bit (bit with a value of 1 or 0) in a Redis string key.

### Method
GET (or equivalent for Redis commands)

### Endpoint
/websites/upstash-redis

### Parameters
#### Query Parameters
- **key** (string) - Required - The key to search in.
- **bit** (0 | 1) - Required - The bit value to search for (0 for clear bit, 1 for set bit).
- **start** (number) - Optional - The index to start searching at.
- **end** (number) - Optional - The index to stop searching at.

### Request Example
```ts
await redis.bitpos("key", 1);
await redis.bitpos("key", 1, 5, 20);
```

### Response
#### Success Response (200)
- **position** (integer) - The index of the first occurrence of the bit in the string. Returns -1 if the bit is not found within the specified range.
```

--------------------------------

### Export Weather API Key

Source: https://upstash.com/docs/redis/tutorials/python_fastapi_caching

Sets the environment variable for the weather API key. This key is required to authenticate requests to the external weather API used in the example.

```shell
export WEATHER_API_KEY=<YOUR_KEY>
```

--------------------------------

### Configure Local Development Backend (Fastly TOML)

Source: https://upstash.com/docs/redis/quickstarts/fastlycompute

This TOML configuration snippet is for the `fastly.toml` file, used to set up the local development server. It defines the 'upstash' backend, mapping it to the Upstash Redis REST URL, enabling local testing of the Fastly service with Redis.

```toml
[local_server.backends.upstash]
url = "UPSTASH_REDIS_REST_URL"
```

--------------------------------

### Setup Cloudflare Worker Project with TypeScript

Source: https://upstash.com/docs/redis/tutorials/cloudflare_workers_with_redis

Initializes a new Cloudflare Worker project using the Wrangler CLI with TypeScript as the language. This sets up the basic project structure and configuration for developing serverless functions on Cloudflare's edge network.

```shell
➜  tutorials > ✗ npx wrangler init
╭ Create an application with Cloudflare Step 1 of 3
│
├ In which directory do you want to create your application?
│ dir ./greetings-cloudflare
│
├ What would you like to start with?
│ category Hello World example
│
├ Which template would you like to use?
│ type Hello World Worker
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
╰ Application created

╭ Configuring your application for Cloudflare Step 2 of 3
│
├ Installing @cloudflare/workers-types
│ installed via npm
│
├ Adding latest types to `tsconfig.json`
│ added @cloudflare/workers-types/2023-07-01
│
├ Retrieving current workerd compatibility date
│ compatibility date 2024-10-22
│
├ Do you want to use git for version control?
│ no git
│
╰ Application configured
```

--------------------------------

### Execute Read-Only Lua Script with EVAL_RO (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/scripts/eval_ro

Demonstrates how to use the EVAL_RO command to execute a read-only Lua script in Python. This example retrieves a value from a Redis key.

```python
script = """
local value = redis.call("GET", KEYS[1])
return value
"""

redis.set("mykey", "Hello")

assert redis.eval_ro(script, keys=["mykey"]) == "Hello"
```

--------------------------------

### Create Serverless Project (Shell)

Source: https://upstash.com/docs/redis/tutorials/job_processing

This snippet shows the initial command to create a new serverless project using the Serverless framework. It prompts for project details and initializes the necessary files for a Node.js AWS Lambda function.

```shell
➜  serverless

Serverless: No project detected. Do you want to create a new one? Yes

Serverless: What do you want to make? AWS Node.js

Serverless: What do you want to call this project? producer

Project successfully created in 'producer' folder.

You can monitor, troubleshoot, and test your new service with a free Serverless account.

Serverless: Would you like to enable this? No

You can run the “serverless” command again if you change your mind later.

```

--------------------------------

### Perform BITOP AND Operation with Redis Python Client

Source: https://upstash.com/docs/redis/sdks/py/commands/bitmap/bitop

This Python code snippet demonstrates how to use the Redis client to perform a BITOP AND operation between two keys ('key1' and 'key2') and store the result in a 'dest' key. It includes setup with SETBIT and assertions to verify the operation's outcome.

```python
redis.setbit("key1", 0, 1)
redis.setbit("key2", 0, 0)
redis.setbit("key2", 1, 1)

assert redis.bitop("AND", "dest", "key1", "key2") == 1

# result = 00000000
assert redis.getbit("dest", 0) == 0
assert redis.getbit("dest", 1) == 0
```

--------------------------------

### Routes with Different Rate Limit Algorithms (JSON)

Source: https://upstash.com/docs/redis/integrations/ratelimit/strapi/configurations

This configuration demonstrates applying different rate limiting algorithms to specific routes. The first strategy uses a 'fixed-window' algorithm for '/api/restaurants/:id', while the second uses a 'tokenBucket' algorithm for '/api/restaurants'. Both identify clients via the 'x-author' header.

```json
{
  "strapi-plugin-upstash-ratelimit": {
    "enabled": true,
    "resolve": "./src/plugins/strapi-plugin-upstash-ratelimit",
    "config": {
      "enabled": true,
      "token": "process.env.UPSTASH_REDIS_REST_TOKEN",
      "url": "process.env.UPSTASH_REDIS_REST_URL",
      "strategy": [
        {
          "methods": ["GET", "POST"],
          "path": "/api/restaurants/:id",
          "identifierSource": "header.x-author",
          "limiter": {
            "algorithm": "fixed-window",
            "tokens": 10,
            "window": "20s"
          }
        },
        {
          "methods": ["GET"],
          "path": "/api/restaurants",
          "identifierSource": "header.x-author",
          "limiter": {
            "algorithm": "tokenBucket",
            "tokens": 10,
            "window": "20s",
            "refillRate": 1
          }
        }
      ],
      "prefix": "@strapi"
    }
  }
}
```

--------------------------------

### ZPOPMAX - Python Example

Source: https://upstash.com/docs/redis/sdks/py/commands/zset/zpopmax

Demonstrates how to use the ZPOPMAX command with Upstash Redis in Python. It first adds members to a sorted set using ZADD and then uses ZPOPMAX to retrieve the member with the highest score. Requires the 'redis' library.

```python
redis.zadd("myset", {"a": 1, "b": 2, "c": 3})

assert redis.zpopmax("myset") == [("c", 3)]
```

--------------------------------

### Python URL Shortener Implementation

Source: https://upstash.com/docs/redis/tutorials/python_url_shortener

A Python script to create a URL shortener using Upstash Redis. It includes functions to generate short codes, shorten URLs by storing them in Redis with an expiration time, and retrieve original URLs. The script uses environment variables for Redis connection and demonstrates example usage.

```python
import string
import random
from upstash_redis import Redis
from dotenv import load_dotenv
import os

# Load environment variables
load_dotenv()

# Redis connection
redis = Redis.from_env()

# Characters to generate the short URL from
CHARS = string.ascii_letters + string.digits
BASE_URL = "https://short.url/"

# Function to generate a random string for the short URL
def generate_short_code(length=6):
    return ''.join(random.choices(CHARS, k=length))

# Function to shorten the URL with an expiration time
def shorten_url(url, expiration=3600):
    # Generate a random short code
    short_code = generate_short_code()
    # Save the short code in Redis
    redis.set(short_code, url, ex=expiration)
    return BASE_URL + short_code

# Function to get the original URL from the short URL
def get_original_url(short_code):
    return redis.get(short_code)

# Example usage
if __name__ == "__main__":
    original_url = "https://example.com/my-very-long-url"

    # Shorten the URL
    short_url = shorten_url(original_url, expiration=600)
    print(f"Shortened URL: {short_url}")

    # Get the original URL
    original_url = get_original_url(short_url.split(\"/\")[-1])

    if original_url:
        print(f"Original URL: {original_url}")
    else:
        print("Short URL expired or not found")
```

--------------------------------

### Redis MGET - Python Example

Source: https://upstash.com/docs/redis/sdks/py/commands/string/mget

Demonstrates how to use the MGET command in Python to retrieve multiple values from Redis. It first sets two key-value pairs and then retrieves their values using MGET, asserting the expected output. This function requires a Redis client instance.

```python
redis.set("key1", "value1")

redis.set("key2", "value2")

assert redis.mget("key1", "key2") == ["value1", "value2"]
```

--------------------------------

### ZPOPMIN Python Example - Upstash Redis

Source: https://upstash.com/docs/redis/sdks/py/commands/zset/zpopmin

Demonstrates how to use the ZPOPMIN command with the Upstash Redis Python client. It first adds elements to a sorted set and then uses ZPOPMIN to retrieve the member with the lowest score. Assumes a Redis client instance is available.

```python
redis.zadd("myset", {"a": 1, "b": 2, "c": 3})

assert redis.zpopmin("myset") == [("a", 1)]
```

--------------------------------

### ZDIFFSTORE Command Example in TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/zset/zdiffstore

Demonstrates how to use the ZDIFFSTORE command in TypeScript with Upstash Redis. This command calculates the difference between specified sets and stores the result in a destination key. It requires the destination key, the number of keys to compare, and the keys themselves as arguments.

```typescript
const values = await redis.zdiffstore("destination", 2, "key1", "key2");
```

--------------------------------

### Serverless Framework Deployment and Invocation Commands

Source: https://upstash.com/docs/redis/tutorials/auto_complete_with_serverless_redis

These shell commands are used to deploy the serverless application and invoke the 'query' function. The deployment command pushes the function to AWS, while the invocation commands demonstrate how to test the function locally and remotely with sample event data.

```shell
serverless deploy
```

```shell
serverless invoke -f query -d '{ "queryStringParameters": {"term":"ca"}}'
```

```shell
serverless invoke local -f query -d '{ "queryStringParameters": {"term":"ca"}}'
```

--------------------------------

### Run Celery Worker

Source: https://upstash.com/docs/redis/integrations/celery

Command to start a Celery worker process. This worker will listen for tasks dispatched to the configured broker (Upstash Redis) and execute them. The '--loglevel=info' flag provides verbose logging.

```bash
celery -A tasks worker --loglevel=info
```

--------------------------------

### Basic Upstash Redis Usage with TypeScript SDK

Source: https://context7.com/context7/upstash-redis/llms.txt

This TypeScript code snippet demonstrates basic string, sorted set, list, hash, and set operations using the Upstash Redis SDK. It shows how to initialize the client with credentials or environment variables and perform common Redis commands.

```typescript
import { Redis } from "@upstash/redis";

// Initialize with credentials
const redis = new Redis({
  url: "https://us1-merry-cat-32748.upstash.io",
  token: "2553feg6a2d9842h2a0gcdb5f8efe9934",
});

// Or load from environment variables
const redis = Redis.fromEnv(); // UPSTASH_REDIS_REST_URL, UPSTASH_REDIS_REST_TOKEN

// String operations
await redis.set("key", "value");
await redis.set("session:abc", "active", { ex: 3600 }); // 1 hour expiration
const data = await redis.get("key");
console.log(data); // "value"

// Sorted sets
await redis.zadd("scores", { score: 100, member: "team1" });
await redis.zadd("scores", { score: 85, member: "team2" });
const topScores = await redis.zrange("scores", 0, 100);
console.log(topScores); // ["team2", "team1"]

// Lists
await redis.lpush("queue", "job1");
await redis.lpush("queue", "job2");
const jobs = await redis.lrange("queue", 0, 10);
console.log(jobs); // ["job2", "job1"]

// Hashes
await redis.hset("user:1001", { name: "alice", age: "30", city: "NYC" });
const name = await redis.hget("user:1001", "name");
console.log(name); // "alice"

// Sets
await redis.sadd("tags", "javascript", "typescript", "node");
const tag = await redis.spop("tags", 1);
console.log(tag); // ["javascript"]
```

--------------------------------

### Get Hash Field TTL with Upstash Redis HTTL (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/hash/httl

This snippet demonstrates how to use the HTTL command with Upstash Redis in TypeScript to retrieve the TTL for a specific field within a hash. It first sets a hash field and an expiration, then calls HTTL to get the remaining seconds. The TTL can be -2 if the field or key does not exist, or -1 if the field exists but has no expiration.

```typescript
await redis.hset("my-key", "my-field", "my-value");
await redis.hexpire("my-key", "my-field", 10);
const ttl = await redis.httl("my-key", "my-field");

console.log(ttl); // e.g., [9]
```

--------------------------------

### HPTTL - Get Hash Field TTL in Milliseconds

Source: https://upstash.com/docs/redis/sdks/ts/commands/hash/hpttl

Retrieves the remaining time-to-live (TTL) for one or more fields within a hash, measured in milliseconds.

```APIDOC
## HPTTL

### Description
Retrieves the remaining time-to-live (TTL) for field(s) in a hash in milliseconds.

### Method
GET

### Endpoint
/websites/upstash-redis

### Parameters
#### Query Parameters
- **key** (string) - Required - The key of the hash.
- **fields** (string | number | (string | number)[]) - Required - The field(s) to retrieve the TTL for.

### Request Example
```json
{
  "key": "my-key",
  "fields": ["my-field1", "my-field2"]
}
```

### Response
#### Success Response (200)
- **ttl_in_milliseconds** (number[]) - The remaining TTL in milliseconds for each field. Returns -2 if the field or key does not exist, or -1 if the field exists but has no expiration.

#### Response Example
```json
{
  "ttl_in_milliseconds": [950, -1]
}
```
```

--------------------------------

### Append entries to a Redis stream with XADD (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/stream/xadd

Appends one or more new entries to a Redis stream using the XADD command. This example demonstrates basic usage and advanced trimming options. It requires the Upstash Redis client library.

```typescript
await redis.xadd(key, "*", { name: "John Doe", age: 30 });
```

```typescript
await redis.xadd(key, "*", { name: "John Doe", age: 30 }, {
  trim: {
    type: "MAXLEN",
    threshold: 1000,
    comparison: "=",
  },
});
```

--------------------------------

### Run SRH via Docker Command

Source: https://upstash.com/docs/redis/sdks/ts/developing

This command starts a Serverless Redis HTTP (SRH) container that connects to a locally running Redis server. SRH will be accessible on port 8080. Ensure you replace 'your_token_here' and 'redis://your_server_here:6379' with your actual token and Redis server details.

```bash
docker run \
    -it -d -p 8080:80 --name srh \
    -e SRH_MODE=env \
    -e SRH_TOKEN=your_token_here \
    -e SRH_CONNECTION_STRING="redis://your_server_here:6379" \
    hiett/serverless-redis-http:latest
```

--------------------------------

### Async Upstash Redis and Pipelines with Python SDK

Source: https://context7.com/context7/upstash-redis/llms.txt

This Python code demonstrates asynchronous operations and pipelining with the Upstash Redis SDK. It shows how to create an async client, perform concurrent GET and INCR operations using asyncio.gather, and efficiently batch multiple commands.

```python
from upstash_redis.asyncio import Redis
import asyncio

# Async client for concurrent operations
redis = Redis.from_env()

async def main():
    # Async operations
    await redis.set("user:1", "alice")
    await redis.set("user:2", "bob")

    # Concurrent operations
    results = await asyncio.gather(
        redis.get("user:1"),
        redis.get("user:2"),
        redis.incr("visit:count")
    )
    print(results)  # ["alice", "bob", 1]

asyncio.run(main())
```

--------------------------------

### HVALS - Get all values from a hash

Source: https://upstash.com/docs/redis/sdks/py/commands/hash/hvals

The HVALS command returns all the values of the members of the hash stored at the specified key. If the hash does not exist, an empty list is returned.

```APIDOC
## GET /websites/upstash-redis/hvals

### Description
Returns all values in the hash stored at key.

### Method
GET

### Endpoint
/websites/upstash-redis/hvals

### Parameters
#### Query Parameters
- **key** (str) - Required - The key of the hash.

### Request Example
```json
{
  "key": "myhash"
}
```

### Response
#### Success Response (200)
- **List[str]** - All values in the hash, or an empty list when key does not exist.

#### Response Example
```json
["Hello", "World"]
```
```

--------------------------------

### Add Members to Redis Set with Python (SADD)

Source: https://upstash.com/docs/redis/sdks/py/commands/set/sadd

Demonstrates how to use the SADD command in Python to add one or more members to a Redis set. The example assumes a 'redis' client is already configured.

```python
assert redis.sadd("key", "a", "b", "c") == 3
```

--------------------------------

### Test API Index Route with cURL

Source: https://upstash.com/docs/redis/tutorials/laravel_caching

This command sends an HTTP GET request to the API endpoint for todos to verify that the API is functioning correctly and returning the expected data.

```shell
curl http://todo-cache.test/api/todos
```

--------------------------------

### SMOVE Example in TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/set/smove

Demonstrates how to use the SMOVE command to move a member from one set to another using the Upstash Redis client. It first adds members to an 'original' set and then moves one member ('a') to the 'destination' set.

```ts
await redis.sadd("original", "a", "b", "c"); 
const moved =  await redis.smove("original", "destination", "a");
// moved:       1
// original:    ["b", "c"]
// destination: ["a"]
```

--------------------------------

### Redis ZDIFFSTORE Python Example

Source: https://upstash.com/docs/redis/sdks/py/commands/zset/zdiffstore

Demonstrates how to use the ZDIFFSTORE command in Python with Upstash Redis. It adds elements to two sorted sets and then computes their difference, storing the result in a new key. The expected output is the count of differing elements.

```python
redis.zadd("key1", {"a": 1, "b": 2, "c": 3})

redis.zadd("key2", {"c": 3, "d": 4, "e": 5})

# a and b
assert redis.zdiffstore("dest", ["key1", "key2"]) == 2
```

--------------------------------

### Upstash Redis HGET Example in TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/hash/hget

This snippet demonstrates how to use the HGET command in Upstash Redis with TypeScript. It first sets a field-value pair using HSET and then retrieves the value using HGET. Ensure the upstash-redis client is initialized before use.

```typescript
await redis.hset("key", {field: "value"});
const field = await redis.hget("key", "field");
console.log(field); // "value"
```

--------------------------------

### GET /get - Retrieve Histogram Data

Source: https://upstash.com/docs/redis/tutorials/histogram

Retrieves the histogram object for a specified name. It fetches the latest latency records from Redis and calculates the histogram.

```APIDOC
## GET /get

### Description
Retrieves the histogram object for a specified name. It fetches the latest latency records from Redis and calculates the histogram.

### Method
GET

### Endpoint
/get

### Parameters
#### Path Parameters
None

#### Query Parameters
- **name** (string) - Required - The name of the histogram to retrieve.

#### Request Body
None

### Request Example
```
GET /get?name=latency_histogram
```

### Response
#### Success Response (200)
- **histogram** (object) - The histogram object containing latency data.

#### Response Example
```json
{
  "histogram": {
    "_counts": [
      [0, 10, 50, 100, 200],
      [0, 2, 5, 8, 10]
    ],
    "_highestTrackableValue": 3600000,
    "_lowestDiscernibleValue": 1,
    "_significantValueDigits": 3,
    "_totalCount": 10
  }
}
```
```

--------------------------------

### Flush Redis Scripts Synchronously

Source: https://upstash.com/docs/redis/sdks/ts/commands/scripts/script_flush

This example demonstrates how to synchronously remove all scripts from the Upstash Redis script cache. This is the default behavior if no options are provided.

```typescript
await redis.scriptFlush();
```

--------------------------------

### GET /lindex

Source: https://upstash.com/docs/redis/sdks/py/commands/list/lindex

Retrieves the element at a specified index within a list stored at a given key. Supports zero-based and negative indexing. Returns None if the index is out of range.

```APIDOC
## GET /lindex

### Description
Returns the element at index `index` in the list stored at key `key`. The index is zero-based. Negative indices can be used to designate elements starting at the tail of the list.

### Method
GET

### Endpoint
/lindex

### Parameters
#### Query Parameters
- **key** (str) - Required - The key of the list.
- **index** (int) - Required - The index of the element to return, zero-based.

### Request Example
```json
{
  "key": "my_list",
  "index": 0
}
```

### Response
#### Success Response (200)
- **value** (Optional[str]) - The value of the element at the specified index. Returns `None` if the index is out of range.

#### Response Example
```json
{
  "value": "element_value"
}
```
```json
{
  "value": null
}
```
```

--------------------------------

### Store Set Difference in New Set (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/set/sdiffstore

This Python example demonstrates how to use the SDIFFSTORE command to find the difference between two sets ('key1' and 'key2') and store the result in a new set named 'res'. It then asserts the expected size of the resulting set and its members.

```python
redis.sadd("key1", "a", "b", "c")

redis.sadd("key2", "c", "d", "e")

# Store the result in a new set
assert redis.sdiffstore("res", "key1", "key2") == 2

assert redis.smembers("set") == {"a", "b"}
```

--------------------------------

### Flush Redis Scripts Asynchronously

Source: https://upstash.com/docs/redis/sdks/ts/commands/scripts/script_flush

This example demonstrates how to asynchronously remove all scripts from the Upstash Redis script cache. It utilizes the 'async: true' option.

```typescript
await redis.scriptFlush({
  async: true,
});
```

--------------------------------

### HVALS - Get All Hash Values

Source: https://upstash.com/docs/redis/sdks/ts/commands/hash/hvals

This endpoint retrieves all values associated with a hash stored at a specified key in Upstash Redis. If the key does not exist, it returns an empty list.

```APIDOC
## GET /websites/upstash-redis/hvals

### Description
Returns all values in the hash stored at key.

### Method
GET

### Endpoint
/websites/upstash-redis/hvals

### Parameters
#### Query Parameters
- **key** (string) - Required - The key of the hash.

### Request Example
```ts
// Example usage with HSET first
await redis.hset("myhash", {
  field1: "value1",
  field2: "value2"
});

// Then retrieve values using HVALS
const values = await redis.hvals("myhash");
console.log(values); // Output: ["value1", "value2"]
```

### Response
#### Success Response (200)
- **values** (string[]) - Required - All values in the hash, or an empty list when key does not exist.

#### Response Example
```json
{
  "values": ["Hello", "World"]
}
```

#### Error Response (404)
- **error** (string) - Not found if the key does not exist.

#### Error Response Example
```json
{
  "error": "Key not found"
}
```
```

--------------------------------

### Create Node.js Express App with Upstash Redis Counter

Source: https://upstash.com/docs/redis/quickstarts/koyeb

This Node.js script sets up an Express server that uses Upstash Redis to increment and display a counter. It requires the `@upstash/redis` and `express` npm packages. The input is an HTTP GET request to the root path, and the output is the current counter value sent as a response.

```javascript
// Note: if you are using Node.js version 17 or lower,
//       change the first line to the following:
// const { Redis } = require ("@upstash/redis/with-fetch");
const { Redis } = require("@upstash/redis");
const express = require("express");

const app = express();
const redis = Redis.fromEnv();

app.get("/", async (req, res) => {
  const value = await redis.get("counter");
  await redis.set("counter", parseInt(value || 0) + 1);
  res.send(`Counter: ${value || 0}`);
});

const PORT = process.env.PORT || 3000;
app.listen(PORT, () => {
  console.log(`Server running on port ${PORT}`);
});
```

--------------------------------

### Create Phoenix App without Ecto (Elixir)

Source: https://upstash.com/docs/redis/quickstarts/elixir

Initializes a new Phoenix project using the 'mix phx.new' command, specifically disabling the default Ecto datastore with the '--no-ecto' flag to utilize Upstash Redis as the primary data store. This is a foundational step for the integration.

```bash
mix phx.new redix_demo --no-ecto 
cd redix_demo
```

--------------------------------

### HRANDFIELD - Get Random Field from Hash

Source: https://upstash.com/docs/redis/sdks/py/commands/hash/hrandfield

Retrieves a single random field from a hash. You can optionally specify if you want to retrieve the value along with the field.

```APIDOC
## GET /websites/upstash-redis/hrandfield

### Description
Returns a random field from a hash.

### Method
GET

### Endpoint
/websites/upstash-redis/hrandfield

### Parameters
#### Query Parameters
- **key** (str) - Required - The key of the hash.
- **count** (int) - Optional - Optionally return more than one field.
- **withvalues** (boolean) - Optional - Return the values of the fields as well.

### Response
#### Success Response (200)
- **response** (Record<str, unknown>) - An object containing the fields and their values.

#### Response Example
```json
{
  "field1": "value1"
}
```
```

--------------------------------

### LTRIM Command

Source: https://upstash.com/docs/redis/sdks/ts/commands/list/ltrim

Trims a list stored at 'key' so that only elements with indices in the range from 'start' to 'end' (inclusive) are retained. Indices are 0-based. Negative indices are supported.

```APIDOC
## LTRIM

### Description
Trims a list stored at 'key' so that only elements with indices in the range from 'start' to 'end' (inclusive) are retained. Indices are 0-based. Negative indices are supported.

### Method
POST

### Endpoint
/websites/upstash-redis

### Parameters
#### Request Body
- **key** (string) - Required - The key of the list.
- **start** (number) - Required - The index of the first element to keep.
- **end** (TValue) - Required - The index of the first element to keep.

### Request Example
```json
{
  "key": "my_list",
  "start": 1,
  "end": 2
}
```

### Response
#### Success Response (200)
- **status** (string) - Returns `OK` if the operation is successful.

#### Response Example
```json
{
  "status": "OK"
}
```
```

--------------------------------

### BITCOUNT with Upstash Redis Client

Source: https://upstash.com/docs/redis/sdks/ts/commands/bitmap/bitcount

Demonstrates how to use the BITCOUNT command with the Upstash Redis client in TypeScript. It shows both the default usage (counting all bits) and usage with specified start and end byte ranges.

```typescript
const bits = await redis.bitcount(key);

```

```typescript
const bits = await redis.bitcount(key, 5, 10);

```

--------------------------------

### Get Key Expiration in Milliseconds (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/generic/pttl

Demonstrates how to use the PTTL command in Python to retrieve the remaining time-to-live for a Redis key in milliseconds. It covers scenarios where the key exists, has an expiration set, and does not have an expiration.

```python
redis.set("key1", "Hello")

assert redis.pttl("key1") == -1

redis.expire("key1", 1000)

assert redis.pttl("key1") > 0

redis.persist("key1")

assert redis.pttl("key1") == -1
```

--------------------------------

### Node.js Express App with Redis Counter

Source: https://upstash.com/docs/redis/quickstarts/fly

A Node.js Express application demonstrating how to connect to a Redis instance and use it to track visitor counts. It installs necessary packages (`express`, `redis`), sets up a Redis client using a provided URL, and defines an endpoint that increments and displays a counter stored in Redis. Dependencies include `express` and `redis`.

```javascript
const express = require("express");
const redis = require("redis");
const { promisify } = require("util");

const app = express();
const client = redis.createClient(process.env.REDIS_URL);

const getAsync = promisify(client.get).bind(client);
const setAsync = promisify(client.set).bind(client);

app.get("/", async (req, res) => {
  const value = await getAsync("counter");
  await setAsync("counter", parseInt(value || 0) + 1);
  res.send(`Hello, visitor number ${value || 0}!`);
});

const PORT = process.env.PORT || 3000;
app.listen(PORT, () => console.log(`Server running on port ${PORT}`));
```

--------------------------------

### Define Project Dependencies (package.json)

Source: https://upstash.com/docs/redis/tutorials/using_serverless_framework

Specifies the project's dependencies in the package.json file. It includes the `@upstash/redis` library, which is essential for interacting with Upstash Redis.

```json
{
    "dependencies": {
      "@upstash/redis": "latest"
    }
  }

```

--------------------------------

### Configure Upstash Redis Environment Variables (Bash)

Source: https://upstash.com/docs/redis/tutorials/python_realtime_chat

Sets up environment variables required to connect to your Upstash Redis instance. This includes the host, port, and password for authentication, ensuring secure and proper connection to the Redis service.

```bash
UPSTASH_REDIS_HOST=your_upstash_redis_host
UPSTASH_REDIS_PORT=your_upstash_redis_port
UPSTASH_REDIS_PASSWORD=your_upstash_redis_password
```

--------------------------------

### Upstash Redis ZADD Python Example

Source: https://upstash.com/docs/redis/sdks/py/commands/zset/zadd

Demonstrates how to use the ZADD command in Python to add multiple elements to a sorted set, and how to use options like NX (only add new), XX (only update existing), GT (greater than), and CH (changed elements).

```python
import redis

redis_client = redis.Redis(host='<your-host>', port=6379, db=0, password='<your-password>')

# Add three elements
assert redis_client.zadd("myset", {
    "one": 1,
    "two": 2,
    "three": 3
}) == 3

# No element is added since "one" and "two" already exist
assert redis_client.zadd("myset", {
    "one": 1,
    "two": 2
}, nx=True) == 0

# New element is not added since it does not exist
assert redis_client.zadd("myset", {
    "new-element": 1
}, xx=True) == 0

# Only "three" is updated since new score was greater
assert redis_client.zadd("myset", {
    "three": 10, "two": 0
}, gt=True) == 1

# Only "three" is updated since new score was greater
assert redis_client.zadd("myset", {
    "three": 10,
    "two": 0
}, gt=True) == 1
```

--------------------------------

### BITFIELD Command

Source: https://upstash.com/docs/redis/sdks/py/commands/bitmap/bitfield

The BITFIELD command allows you to perform multiple bitfield operations (get, set, incr) in a single atomic command. It returns a list of integers, one for each operation performed.

```APIDOC
## BITFIELD

### Description
Sets or gets parts of a bitfield. The `bitfield` function returns a `BitFieldCommands` instance that can be used to execute multiple bitfield operations in a single command.

### Method
BITFIELD

### Endpoint
`/websites/upstash-redis (Conceptual - BITFIELD is a Redis command)

### Parameters
#### Path Parameters
None

#### Query Parameters
None

#### Request Body
- **key** (str) - Required - The string key to operate on.
- **operations** (List[Dict]) - Required - A list of operations to perform. Each operation is a dictionary with 'type', 'offset', and potentially 'value' or 'increment'.
  - **type** (str) - Required - The encoding type (e.g., 'i4', 'u8').
  - **offset** (int) - Required - The bit offset to operate on.
  - **value** (int) - Optional - The value to set (for 'set' operation).
  - **increment** (int) - Optional - The value to increment by (for 'incr' operation).

### Request Example
```json
{
  "key": "mykey",
  "operations": [
    {"type": "u4", "offset": 0, "value": 16},
    {"type": "u4", "offset": 4, "increment": 1}
  ]
}
```

### Response
#### Success Response (200)
- **result** (List[int]) - Required - A list of integers, one for each operation performed.

#### Response Example
```json
{
  "result": [0, 1]
}
```

## Commands

### `get(type: str, offset: int)`

Returns a value from the bitfield at the given offset.

### `set(type: str, offset: int, value: int)`

Sets a value and returns the old value.

### `incr(type: str, offset: int, increment: int)`

Increments a value and returns the new value.

## Arguments

<ParamField body="key" type="str" required>
  The string key to operate on.
</ParamField>

## Response

<ResponseField type="List[int]" required>
  A list of integers, one for each operation.
</ResponseField>

```

--------------------------------

### Run and Deploy SST Application

Source: https://upstash.com/docs/redis/quickstarts/ion

Commands to run the Next.js application locally for development and to deploy the application using SST. These commands initiate the local development server and the cloud deployment process.

```shell
npm run dev
sst deploy
```

--------------------------------

### Successful Redis Command Execution Response

Source: https://upstash.com/docs/redis/features/restapi

Example of a successful JSON response from the Upstash REST API. The response contains a single 'result' field with the value returned by the Redis command.

```json
{ "result": "OK" }
{ "result": null }
{ "result": 137 }
{ "result": "value" }
{ "result": ["value1", null, "value2"] }
```

--------------------------------

### Serverless Framework Configuration

Source: https://upstash.com/docs/redis/tutorials/auto_complete_with_serverless_redis

A basic serverless.yml file for configuring a Serverless Framework project. It defines the service name and is intended to be extended with function definitions, provider settings, and plugins for deployment.

```yaml
service: auto-complete-api

```

--------------------------------

### Python Redis ZINCRBY Example

Source: https://upstash.com/docs/redis/sdks/py/commands/zset/zincrby

This snippet demonstrates how to use the ZINCRBY command with the Python Upstash Redis client. It first adds members to a sorted set and then increments the score of an existing member, asserting the new score.

```python
redis.zadd("myset", {"one": 1, "two": 2, "three": 3})

assert redis.zincrby("myset", 2, "one") == 3
```

--------------------------------

### Error Response from Redis Command Execution

Source: https://upstash.com/docs/redis/features/restapi

Example of an error JSON response from the Upstash REST API when a command fails or is rejected. The response contains a single 'error' field with a descriptive message.

```json
{"error":"WRONGPASS invalid password"}
{"error":"ERR wrong number of arguments for 'get' command"}
```

--------------------------------

### Set Expiration Time with EXPIREAT (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/generic/expireat

Demonstrates how to set a key in Upstash Redis and then set an expiration time for it using the EXPIREAT command with a Unix timestamp. This example requires the 'redis' client library.

```typescript
await redis.set("mykey", "Hello");
const tenSecondsFromNow = Math.floor(Date.now() / 1000) + 10;
await redis.expireat("mykey", tenSecondsFromNow);
```

--------------------------------

### Connect to Upstash Redis using Redisson in Java

Source: https://upstash.com/docs/redis/tutorials/redisson

This Java code demonstrates how to configure and connect to an Upstash Redis database using the Redisson client. Replace 'YOUR_PASSWORD' and 'YOUR_ENDPOINT' with your actual Upstash credentials. The endpoint should start with 'rediss://' if TLS is enabled.

```java
import org.redisson.Redisson;
import org.redisson.api.RMap;
import org.redisson.api.RedissonClient;
import org.redisson.config.Config;

public class Main {

    public static void main(String[] args) {
        Config config = new Config();
        config.useSingleServer().setPassword("YOUR_PASSWORD")
                // use "rediss://" for SSL connection
                .setAddress("YOUR_ENDPOINT");
        RedissonClient redisson = Redisson.create(config);
        RMap<String, String> map = redisson.getMap("map");
        map.put("foo", "bar");
        System.out.println(map.get("foo"));
    }
}
```

--------------------------------

### XRANGE Command

Source: https://upstash.com/docs/redis/sdks/ts/commands/stream/xrange

Retrieves stream entries from a Redis stream that fall within a given range of IDs. It supports specifying a key, start and end IDs, and an optional count for limiting the results.

```APIDOC
## XRANGE Command

### Description
Returns stream entries matching a given range of IDs.

### Method
GET (conceptual, as it's a command on a data store)

### Endpoint
`/websites/upstash-redis/xrange` (conceptual endpoint for the command)

### Parameters
#### Query Parameters
- **key** (string) - Required - The key of the stream.
- **start** (string) - Required - The stream entry ID to start from.
- **end** (string) - Required - The stream entry ID to end at.
- **count** (integer) - Optional - The maximum number of entries to return.

### Request Example
```json
{
  "key": "my-stream",
  "start": "-",
  "end": "+",
  "count": 10
}
```

### Response
#### Success Response (200)
- **Record<streamId, Record<field, value>>** - An object of stream entries, keyed by their stream ID.

#### Response Example
```json
{
  "1548149259438-0": {
    "field1": "value1",
    "field2": "value2"
  },
  "1548149259438-1": {
    "field1": "value3",
    "field2": "value4"
  }
}
```
```

--------------------------------

### Upstash Create Database API (cURL)

Source: https://upstash.com/docs/redis/help/integration

An example cURL request to the Upstash API for creating a new Redis database. It uses basic authentication with email and API key, and a JSON payload to specify database details like name, region, and read regions.

```bash
curl -X POST \
  https://api.upstash.com/v2/redis/database \
  -u 'EMAIL:API_KEY' \
  -d '{"name":"myredis", "region":"global", "primary_region":"us-east-1", "read_regions":["us-west-1","us-west-2"], "tls": true}'
```

--------------------------------

### Get Hash Field Count with Python (Upstash Redis)

Source: https://upstash.com/docs/redis/sdks/py/commands/hash/hlen

Demonstrates how to use the HLEN command with Upstash Redis in Python to retrieve the number of fields in a hash. It includes setting fields using HSET and then verifying the count with HLEN.

```python
assert redis.hlen("myhash") == 0

redis.hset("myhash", values={
    "field1": "Hello",
    "field2": "World"
})

assert redis.hlen("myhash") == 2
```

--------------------------------

### Perform Set Difference and Store in New Set (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/set/sdiffstore

This example demonstrates how to use the `sdiffstore` command in Upstash Redis using TypeScript. It first adds members to two sets and then calculates the difference, storing the result in a new set named 'dest'. The command requires the destination key and the keys of the source sets.

```typescript
await redis.sadd("set1", "a", "b", "c"); 
await redis.sadd("set2", "c", "d", "e"); 
await redis.sdiffstore("dest", "set1", "set2");
// The 'dest' set will contain ['a', 'b']
```

--------------------------------

### Laravel Cache::remember Method Example

Source: https://upstash.com/docs/redis/tutorials/laravel_caching

Demonstrates the usage of Laravel's `Cache::remember` method. It attempts to retrieve data from the cache using the key 'todos'. If the key doesn't exist, it executes the provided closure (fetching all todos) and stores the result in the cache for a specified duration.

```php
$value = Cache::remember('todos', $seconds, function () {
    return Todo::all();
});

```

--------------------------------

### Configure Upstash Redis Environment Variables for Cloudflare Worker

Source: https://upstash.com/docs/redis/tutorials/cloudflare_websockets_redis

This snippet shows how to set up environment variables in the `wrangler.toml` file for a Cloudflare Worker to connect to an Upstash Redis database. It requires the Redis URL and token, which are sensitive credentials.

```toml
name = "chat-app"
main = "src/index.ts"
compatibility_date = "2024-01-01"

[vars]
UPSTASH_REDIS_REST_URL = "YOUR_REDIS_URL"
UPSTASH_REDIS_REST_TOKEN = "YOUR_REDIS_TOKEN"
```

--------------------------------

### Strategy Configuration

Source: https://upstash.com/docs/redis/integrations/ratelimit/strapi/configurations

Define rate limits and algorithms for specific routes.

```APIDOC
## Strategy Configuration

### Description
Define rate limits per route using a strategy array. Each strategy object specifies methods, paths, identifier sources, and limiter configurations.

### Parameters
#### Request Body
- **strategy** (array) - Required - An array of strategy objects.
  - **methods** (array of strings) - Required - HTTP methods to apply the rate limit (e.g., `['GET', 'POST']`).
  - **path** (string) - Required - The path to apply the rate limit. Wildcards are supported (e.g., `*`, `/api/restaurants/:id`).
  - **identifierSource** (string) - Required - Source to identify the user for rate limiting (e.g., `ip`, `header.<HEADER_KEY>`).
  - **debug** (boolean) - Optional - Enable debug mode for the route. Logs remaining limits and block status.
  - **limiter** (object) - Required - The limiter configuration.
    - **algorithm** (string: `'fixed-window' | 'sliding-window' | 'token-bucket'`) - Required - The rate limit algorithm to use.
    - **tokens** (number) - Required - The number of tokens allowed in the time window.
    - **window** (string) - Required - The time window for the rate limit (e.g., `20s`, `1h`). Units: `ms`, `s`, `m`, `h`, `d`.
    - **refillRate** (number) - Optional - The rate at which the bucket refills (only for `token-bucket` algorithm).

### Request Example
```json
{
  "strategy": [
    {
      "methods": ["GET", "POST"],
      "path": "/api/products/:id",
      "identifierSource": "ip",
      "debug": true,
      "limiter": {
        "algorithm": "sliding-window",
        "tokens": 100,
        "window": "1m"
      }
    },
    {
      "methods": ["ALL"],
      "path": "/api/auth/*",
      "identifierSource": "header.Authorization",
      "limiter": {
        "algorithm": "fixed-window",
        "tokens": 10,
        "window": "1h"
      }
    }
  ]
}
```

### Response
#### Success Response (200)
- **message** (string) - Confirmation message.

#### Response Example
```json
{
  "message": "Strategy configurations updated successfully."
}
```
```

--------------------------------

### Python Example: Trim Redis List with LTRIM

Source: https://upstash.com/docs/redis/sdks/py/commands/list/ltrim

Demonstrates how to use the LTRIM command in Python to trim a Redis list. It first pushes elements to a list and then uses LTRIM to keep only the first two elements. Asserts the trimming operation's success and the final state of the list.

```python
redis.rpush("mylist", "one", "two", "three")

assert redis.ltrim("mylist", 0, 1) == True

assert redis.lrange("mylist", 0, -1) == ["one", "two"]
```

--------------------------------

### Configure Upstash Redis Credentials in wrangler.toml or wrangler.jsonc

Source: https://upstash.com/docs/redis/quickstarts/cloudflareworkers

Demonstrates how to configure Upstash Redis connection credentials (URL and Token) within the Cloudflare Wrangler configuration files. These variables are used by the worker to establish a connection to the Redis instance.

```yaml
[vars]
UPSTASH_REDIS_REST_URL="REPLACE_HERE"
UPSTASH_REDIS_REST_TOKEN="REPLACE_HERE"

```

```json
{
  "vars": {
    "UPSTASH_REDIS_REST_URL": "REPLACE_HERE",
    "UPSTASH_REDIS_REST_TOKEN": "REPLACE_HERE"
  }
}

```

--------------------------------

### HGET - Retrieve Hash Field Value

Source: https://upstash.com/docs/redis/sdks/ts/commands/hash/hget

This section details the HGET command for retrieving the value associated with a specific field within a Redis hash. It includes parameter descriptions, expected responses, and illustrative examples.

```APIDOC
## HGET

### Description
Retrieves the value of a hash field.

### Method
GET

### Endpoint
`/websites/upstash-redis

### Parameters
#### Path Parameters
- **key** (string) - Required - The key to get.
- **field** (string) - Required - The field to get.

### Request Example
```json
{
  "key": "your_key",
  "field": "your_field"
}
```

### Response
#### Success Response (200)
- **TValue | null** (any) - The value of the field, or `null`, when field is not present in the hash or key does not exist.

#### Response Example
```json
{
  "value": "retrieved_value"
}
```
```

--------------------------------

### Run Cloudflare Worker Locally with Wrangler

Source: https://upstash.com/docs/redis/tutorials/cloudflare_workers_with_redis

Starts a local development server for the Cloudflare Worker using the Wrangler CLI. This command allows you to test your worker function and its integration with Upstash Redis on your local machine before deployment.

```shell
npx wrangler dev
```

--------------------------------

### Remove Elements from Sorted Set by Rank (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/zset/zremrangebyrank

This TypeScript example demonstrates how to use the ZREMRANGEBYRANK command to remove elements from a sorted set between specified ranks. It requires an initialized Redis client instance.

```typescript
await redis.zremrangebyrank("key", 4, 20)
```

--------------------------------

### Execute Read-Only Lua Script with Arguments using EVAL_RO (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/scripts/eval_ro

Shows how to pass arguments to a read-only Lua script executed via the EVAL_RO command in Python. This example returns the first argument passed to the script.

```python
assert redis.eval_ro("return ARGV[1]", args=["Hello"]) == "Hello"
```

--------------------------------

### Sliding Window Rate Limiter Approximation (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ratelimit-ts/algorithms

Demonstrates the approximation logic for the Sliding Window rate limiting algorithm. This algorithm uses a rolling window for more accurate rate limiting than Fixed Window but is more computationally expensive. The example shows how to calculate the effective rate based on requests in the current and previous windows.

```typescript
let limit = 10;

// 4 request from the old window, weighted + requests in current window
const rate = 4 * ((60 - 15) / 60) + 5;

return rate < limit // True means we should allow the request
```

--------------------------------

### JSON.MGET - Get multiple JSON values

Source: https://upstash.com/docs/redis/sdks/py/commands/json/mget

The JSON.MGET command retrieves the same path from multiple JSON documents stored in Redis. It takes a list of keys and a JSON path as arguments and returns a list of the values found at that path in each document.

```APIDOC
## JSON.MGET

### Description
Get the same path from multiple JSON documents.

### Method
N/A (This is a Redis command, not a typical HTTP API endpoint)

### Endpoint
N/A

### Parameters
#### Path Parameters
None

#### Query Parameters
None

#### Request Body
* **keys** (List[str]) - Required - One or more keys of JSON documents.
* **path** (str) - Required - The path to get from the JSON document.

### Request Example
```py
redis.json.mget(["key1", "key2"],  "$.path.to.somewhere")
```

### Response
#### Success Response (200)
* **values** (List[List[TValue]]) - The values at the specified path or `null` if the path does not exist.

#### Response Example
```json
[
  [
    "value1",
    "value2"
  ]
]
```
```

--------------------------------

### Create New Laravel Project and Navigate

Source: https://upstash.com/docs/redis/tutorials/laravel_caching

This command initializes a new Laravel project and changes the directory into the newly created project folder. It's the foundational step for any new Laravel application.

```shell
laravel new todo-cache
cd todo-cache
```

--------------------------------

### Retrieve List Elements with LRANGE in Python

Source: https://upstash.com/docs/redis/sdks/py/commands/list/lrange

Demonstrates how to use the LRANGE command in Python to fetch elements from a Redis list. It shows examples of retrieving a specific range and the entire list using positive and negative indices. Assumes a Redis client object named 'redis' is already configured.

```python
redis.rpush("mylist", "one", "two", "three")

assert redis.lrange("mylist", 0, 1) == ["one", "two"]

assert redis.lrange("mylist", 0, -1) == ["one", "two", "three"]
```

--------------------------------

### JSON.GET - Get a single value from a JSON document

Source: https://upstash.com/docs/redis/sdks/py/commands/json/get

The JSON.GET command retrieves a single value from a JSON document stored in Redis. You can specify the key of the JSON entry and one or more paths to extract the desired data.

```APIDOC
## GET /websites/upstash-redis/json/get

### Description
Retrieves a single value from a JSON document stored in Redis using the JSON.GET command. Specify the key and the path(s) to the desired value(s).

### Method
GET

### Endpoint
/websites/upstash-redis/json/get

### Parameters
#### Query Parameters
- **key** (str) - Required - The key of the JSON entry.
- **paths** (*List[str]) - Optional - Defaults to "$". One or more paths to retrieve from the JSON document.

### Request Example
```py
redis.json.get("key", "$.path.to.somewhere")
```

### Response
#### Success Response (200)
- **value** (List[TValue | null]) - The value at the specified path or `null` if the path does not exist.
```

--------------------------------

### Get JSON Value with Options using Upstash Redis Client (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/json/get

Illustrates how to use the JSON.GET command with optional formatting arguments provided by the Upstash Redis client. This allows for custom indentation, newlines, and spacing in the returned JSON snippet.

```typescript
const value = await redis.json.get("key", {
    indent: "  ",
    newline: "\n",
    space: " ",
}, "$.path.to.somewhere");
```

--------------------------------

### Scan Set Members with Python

Source: https://upstash.com/docs/redis/sdks/py/commands/set/sscan

This Python example demonstrates how to scan all members of a set using the SSCAN command. It handles pagination by repeatedly calling SSCAN with the returned cursor until the cursor value becomes 0, indicating the scan is complete. The `match` option can be used to filter members based on a glob-style pattern.

```python
cursor = 0
results = set()

while True:
    cursor, keys = redis.sscan("myset", cursor, match="*")

    results.extend(keys)
    if cursor == 0:
        break
```

--------------------------------

### General Configurations

Source: https://upstash.com/docs/redis/integrations/ratelimit/strapi/configurations

Configure global settings for the Upstash Redis Rate Limiter Strapi Plugin.

```APIDOC
## General Configurations

### Description
Enable or disable the rate limiter plugin globally.

### Parameters
#### Request Body
- **enabled** (boolean) - Optional - Default: `true` - Enable or disable the plugin.

### Request Example
```json
{
  "enabled": true
}
```

### Response
#### Success Response (200)
- **message** (string) - Confirmation message.

#### Response Example
```json
{
  "message": "Plugin settings updated successfully."
}
```
```

--------------------------------

### Get Random Field from Hash (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/hash/hrandfield

This snippet demonstrates how to retrieve a single random field from a Redis hash using the Upstash Python SDK. It assumes a hash named 'myhash' has been populated with fields.

```python
redis.hset("myhash", values={
    "field1": "Hello",
    "field2": "World"
})

assert redis.hrandfield("myhash") in ["field1", "field2"]
```

--------------------------------

### Create Java Maven Project with Serverless Framework

Source: https://upstash.com/docs/redis/tutorials/serverless_java_redis

Creates a new AWS Java Maven project using the Serverless Framework. This sets up the basic structure for a serverless Java application.

```shell
serverless create --template aws-java-maven --name counter-api -p aws-java-counter-api
```

--------------------------------

### Set Bit in Redis using TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/bitmap/setbit

This TypeScript example demonstrates how to use the `setbit` command with Upstash Redis. It requires a Redis client instance and specifies the key, offset, and the new bit value. The command returns the previous value of the bit at the given offset.

```typescript
const originalBit = await redis.setbit(key, 4, 1);
```

--------------------------------

### Node.js Histogram API Handler with Redis and ioredis

Source: https://upstash.com/docs/redis/tutorials/histogram

Implements the serverless functions for the histogram API. The `get` function retrieves latency data from a Redis list, builds a histogram using `hdr-histogram-js`, and returns it. The `record` function accepts latency values and pushes them into a Redis list. A helper function `fixUrl` ensures correct Redis URL formatting.

```javascript
const hdr = require("hdr-histogram-js");
const Redis = require("ioredis");
if (typeof client === "undefined") {
  var client = new Redis(fixUrl(process.env.REDIS_URL));
}
const headers = {
  "Access-Control-Allow-Origin": "*",
  "Access-Control-Allow-Credentials": true,
};
const SIZE = 10000;

module.exports.get = async (event) => {
  if (!event.queryStringParameters || !event.queryStringParameters.name) {
    return {
      statusCode: 400,
      headers: headers,
      body: JSON.stringify({
        message: "Invalid parameters. Name is needed.",
      }),
    };
  }
  const name = event.queryStringParameters.name;
  const data = await client.lrange(name, 0, SIZE);
  const histogram = hdr.build();
  data.forEach((item) => {
    histogram.recordValue(item);
  });

  return {
    statusCode: 200,
    body: JSON.stringify({
      histogram: histogram,
    }),
  };
};

module.exports.record = async (event) => {
  let body = JSON.parse(event.body);
  if (!body || !body.name || !body.values) {
    return {
      statusCode: 400,
      headers: headers,
      body: JSON.stringify({
        message: "Invalid parameters. Name and values are needed.",
      }),
    };
  }
  const name = body.name;
  const values = body.values;
  await client.lpush(name, values);
  return {
    statusCode: 200,
    body: JSON.stringify({
      message: "Success",
      name: name,
    }),
  };
};

function fixUrl(url) {
  if (!url) {
    return "";
  }
  if (url.startsWith("redis://") && !url.startsWith("redis://:")) {
    return url.replace("redis://", "redis://:");
  }
  if (url.startsWith("rediss://") && !url.startsWith("rediss://:")) {
    return url.replace("rediss://", "rediss://:");
  }
  return url;
}
```

--------------------------------

### Export Data to File using upstash-redis-dump

Source: https://upstash.com/docs/redis/howto/importexport

This command exports data from a specified Redis database (db 0) to a file named 'redis.dump'. It connects to a remote Redis instance using its host, port, and password, and utilizes TLS for secure communication. Ensure you have the upstash-redis-dump tool installed and replace 'PASSWORD' with your actual database password.

```shell
$ upstash-redis-dump -db 0 -host eu1-moving-loon-6379.upstash.io -port 6379 -pass PASSWORD -tls > redis.dump
```

--------------------------------

### Cloudflare Workers Redis Client Setup

Source: https://upstash.com/docs/redis/sdks/ts/deployment

Configures the Upstash Redis client specifically for Cloudflare Workers. Environment variables should be set using `wrangler secret put`. The client can be instantiated with explicit credentials or loaded from the global environment, with variations for service and module workers.

```typescript
import { Redis } from "@upstash/redis/cloudflare"

const redis = new Redis({
  url: <UPSTASH_REDIS_REST_URL>,
  token: <UPSTASH_REDIS_REST_TOKEN>,
})


// or load directly from global env

// service worker
const redis = Redis.fromEnv()


// module worker
export default {
  async fetch(request: Request, env: Bindings) {
    const redis = Redis.fromEnv(env)
    // ...
  }
}
```

--------------------------------

### Create Upstash Redis Instance using Fly CLI

Source: https://upstash.com/docs/redis/quickstarts/fly

This shell command initiates the creation of a new Upstash Redis database through the Fly CLI. It prompts the user for organization, database name, primary region, and eviction policy. The output provides the connection URL for the newly created Redis instance.

```shell
> flyctl redis create
? Select Organization: upstash (upstash)
? Choose a Redis database name (leave blank to generate one):
? Choose a primary region (can't be changed later) San Jose, California (US) (sjc)

Upstash Redis can evict objects when memory is full. This is useful when caching in Redis. This setting can be changed later.
Learn more at https://fly.io/docs/reference/redis/#memory-limits-and-object-eviction-policies
? Would you like to enable eviction? No
? Optionally, choose one or more replica regions (can be changed later):
? Select an Upstash Redis plan 3G: 3 GB Max Data Size

Your Upstash Redis database silent-tree-6201 is ready.
Apps in the upstash org can connect to at redis://default:978ba2e07tyrt67598acd8ac916a@fly-silent-tree-6201.upstash.io
If you have redis-cli installed, use fly redis connect to connect to your database.
```

--------------------------------

### Get Random Field from Hash (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/hash/hrandfield

Retrieves a single random field from a specified hash key. This is the basic usage of the HRANDFIELD command. It requires a valid Redis key. The output is a string representing the field name.

```typescript
await redis.hset("key", {
  id: 1,
  username: "chronark",
  name: "andreas"
 });
const randomField = await redis.hrandfield("key");
console.log(randomField); // one of "id", "username" or  "name"
```

--------------------------------

### Basic Upstash Redis Usage with Python SDK

Source: https://context7.com/context7/upstash-redis/llms.txt

This Python code snippet illustrates fundamental operations with the Upstash Redis SDK, including string manipulation, incrementing counters, hash operations, and list management. It shows initialization using direct credentials or environment variables and executing custom commands.

```python
from upstash_redis import Redis

# Initialize with credentials
redis = Redis(
    url="https://us1-merry-cat-32748.upstash.io",
    token="2553feg6a2d9842h2a0gcdb5f8efe9934"
)

# Or load from environment variables
redis = Redis.from_env()  # UPSTASH_REDIS_REST_URL, UPSTASH_REDIS_REST_TOKEN

# String operations
redis.set("key", "value")
redis.set("counter", 0)
print(redis.get("key"))  # "value"

# Increment operations
redis.incr("counter")
redis.incr("counter")
print(redis.get("counter"))  # "2"

# Hash operations
redis.hset("product:1001", {"name": "laptop", "price": "999", "stock": "50"})
price = redis.hget("product:1001", "price")
print(price)  # "999"

# Lists
redis.lpush("notifications", "msg1")
redis.lpush("notifications", "msg2")
messages = redis.lrange("notifications", 0, 10)
print(messages)  # ["msg2", "msg1"]

# Custom commands not implemented in SDK
result = redis.execute(["XLEN", "stream:events"])
print(result)
```

--------------------------------

### Deploy Serverless Service

Source: https://upstash.com/docs/redis/tutorials/using_serverless_framework

Deploys the Serverless Framework service to AWS Lambda. This command packages the code, creates the necessary AWS resources, and makes the API endpoint available.

```shell
serverless deploy

```

--------------------------------

### Get JSON Value Type with Python

Source: https://upstash.com/docs/redis/sdks/py/commands/json/type

This Python code snippet demonstrates how to use the `redis.json.type` command to retrieve the type of a JSON value stored under a specific key and path in Upstash Redis. It requires the `redis-py` library.

```python
myType = redis.json.type("key", "$.path.to.value")
```

--------------------------------

### Python LINSERT Example - Upstash Redis

Source: https://upstash.com/docs/redis/sdks/py/commands/list/linsert

This Python code snippet demonstrates how to use the LINSERT command with Upstash Redis. It first pushes elements 'a', 'b', and 'c' into a list associated with the key 'key'. Then, it inserts the element 'x' before the pivot element 'b' in the same list. This operation is useful for modifying lists in place.

```python
redis.rpush("key", "a", "b", "c")
redis.linsert("key", "before", "b", "x")
```

--------------------------------

### Python Redis SINTER Example

Source: https://upstash.com/docs/redis/sdks/py/commands/set/sinterstore

This Python code snippet demonstrates how to use the Upstash Redis SINTER command. It first adds elements to two sets, 'set1' and 'set2', and then performs an intersection operation, storing the result in 'destination'. The assertion verifies that the intersection contains exactly one element.

```python
redis.sadd("set1", "a", "b", "c"); 

redis.sadd("set2", "c", "d", "e"); 

assert redis.sinter("destination", "set1", "set2") == 1
```

--------------------------------

### Example of Upstash Redis LMOVE Command in TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/list/lmove

This snippet demonstrates how to use the `redis.move` command in TypeScript. It first pushes elements 'a', 'b', and 'c' to the 'source' list using `rpush`, then moves an element from the left side of 'source' to the left side of 'destination'. The moved element is stored in the `element` variable.

```typescript
await redis.rpush("source", "a", "b", "c"); 
const element = await redis.move("source", "destination", "left", "left");
```

--------------------------------

### Upstash OAuth 2.0 Authorization URL

Source: https://upstash.com/docs/redis/help/integration

This is the authorization URL initiated by the web app to start the Upstash OAuth 2.0 flow. It includes parameters like response type, audience, scope, client ID, and redirect URI.

```plaintext
https://auth.upstash.com/authorize?response_type=code&audience=upstash-api&scope=offline_access&client_id=XXXXXXXXXX&redirect_uri=http%3A%2F%2Flocalhost:3000
```

--------------------------------

### Deploy Phoenix App Changes on Fly

Source: https://upstash.com/docs/redis/quickstarts/elixir

After launching and configuring the application on Fly.io, this command deploys the latest changes. It updates the application on the Fly.io infrastructure. This command should be run after making any code modifications or configuration updates.

```bash
fly deploy
```

--------------------------------

### Node.js Dockerfile for Koyeb Deployment

Source: https://upstash.com/docs/redis/quickstarts/koyeb

A Dockerfile designed to build a Node.js application for deployment on Koyeb. It includes multi-stage builds for optimizing image size and sets up the necessary environment for running the application.

```dockerfile
FROM node:18-alpine AS base

FROM base AS deps
RUN apk add --no-cache libc6-compat
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci

FROM base AS runner
WORKDIR /app
RUN addgroup --system --gid 1001 nodejs
RUN adduser --system --uid 1001 nodejs
COPY --from=deps /app/node_modules ./
COPY . .
USER node
EXPOSE 3000
ENV PORT 3000
CMD ["npm", "run", "start"]
```

--------------------------------

### Trim List with LTRIM in TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/list/ltrim

This example demonstrates how to use the LTRIM command in TypeScript to trim a Redis list. It first pushes elements to a list and then trims it to keep elements between index 1 and 2 (inclusive). The list is modified in-place.

```ts
await redis.lpush("key", "a", "b", "c", "d"); 
await redis.ltrim("key", 1, 2); 
// the list is now ["b", "c"]
```

--------------------------------

### Get Remaining Rate Limit Tokens (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ratelimit-ts/methods

This method retrieves the number of remaining tokens and the reset timestamp for a given identifier. It returns a Promise that resolves to an object containing 'remaining' (number of tokens) and 'reset' (reset timestamp).

```typescript
ratelimit.getRemaining(identifier: string): Promise<{ \n  remaining: number;\n  reset: number;\n}>
```

--------------------------------

### Build Container Image with gcloud

Source: https://upstash.com/docs/redis/tutorials/cloud_run_sessions

This command builds a Docker container image for your application and tags it for Google Container Registry. It assumes you have a Dockerfile in your project directory. The image is tagged with a specific name and project ID.

```bash
gcloud builds submit --tag gcr.io/cloud-run-sessions/main
```

--------------------------------

### Set List Value at Index (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/list/lset

This example demonstrates how to use the LSET command in Upstash Redis with TypeScript to set a value at a specific index in a list. It first pushes elements to a list and then updates an element at index 1.

```ts
await redis.lpush("key", "a", "b", "c"); 
await redis.lset("key", 1, "d"); 

// list is now ["a", "d", "c"]
```

--------------------------------

### Configure Upstash Ratelimit Plugin in Strapi

Source: https://upstash.com/docs/redis/integrations/ratelimit/strapi/getting-started

Configure the Upstash Ratelimit plugin in your Strapi project by setting environment variables and defining rate limiting strategies. This involves specifying the Redis URL and token, as well as the desired rate limiting algorithms, token counts, and time windows.

```typescript
export default () => ({
  "strapi-plugin-upstash-ratelimit": {
    enabled: true,
    resolve: "./src/plugins/strapi-plugin-upstash-ratelimit",
    config: {
      enabled: true,
      token: process.env.UPSTASH_REDIS_REST_TOKEN,
      url: process.env.UPSTASH_REDIS_REST_URL,
      strategy: [
        {
          methods: ["GET", "POST"],
          path: "*",
          limiter: {
            algorithm: "fixed-window",
            tokens: 10,
            window: "20s",
          },
        },
      ],
      prefix: "@strapi",
    },
  },
});
```

```javascript
module.exports = () => ({
  "strapi-plugin-upstash-ratelimit": {
    enabled: true,
    resolve: "./src/plugins/strapi-plugin-upstash-ratelimit",
    config: {
      enabled: true,
      token: process.env.UPSTASH_REDIS_REST_TOKEN,
      url: process.env.UPSTASH_REDIS_REST_URL,
      strategy: [
        {
          methods: ["GET", "POST"],
          path: "*",
          limiter: {
            algorithm: "fixed-window",
            tokens: 10,
            window: "20s",
          },
        },
      ],
      prefix: "@strapi",
    },
  },
});
```

--------------------------------

### Check Request Against Deny List with Ratelimit

Source: https://upstash.com/docs/redis/sdks/ratelimit-ts/traffic-protection

This example shows how to call the `limit` method on the Ratelimit client, providing details like IP address, user agent, and country. The client will automatically check these against the configured deny list. If a match is found, the request is blocked, and the `success` property will be `false`, with `reason` set to "denyList".

```tsx
const { success, pending, reason, deniedValue } = ratelimit.limit("userId", {
  ip: "ip-address",
  userAgent: "user-agent",
  country: "country",
});

await pending; // await pending if you have analytics enabled

console.log(success, reason, deniedValue);
// prints: false, "denyList", "ip-address"
```

--------------------------------

### Get TTL of a Key in Python

Source: https://upstash.com/docs/redis/sdks/py/commands/generic/ttl

This Python code snippet demonstrates how to use the TTL command with Upstash Redis. It shows setting a key, checking its TTL when it has no expiration, setting an expiration, and then checking the TTL again. It also includes a check for a non-existent key.

```python
# Get the TTL of a key
redis.set("my-key", "value")

assert redis.ttl("my-key") == -1

redis.expire("my-key", 10)

assert redis.ttl("my-key") > 0

# Non existent key
assert redis.ttl("non-existent-key") == -2
```

--------------------------------

### Build Project with Maven

Source: https://upstash.com/docs/redis/tutorials/serverless_java_redis

Builds the Java project using Apache Maven. This command compiles the code, runs tests, and packages the application into a JAR file, typically in the target directory.

```shell
mvn clean install
```

--------------------------------

### Get JSON Object Keys with Python (Upstash Redis)

Source: https://upstash.com/docs/redis/sdks/py/commands/json/objkeys

This snippet demonstrates how to use the JSON.OBJKEYS command with Python to retrieve keys from a JSON object stored in Upstash Redis. It requires the 'redis' library and provides the key and path to the JSON object as input.

```python
import redis

redis_client = redis.Redis(
    host="your_host",
    port=your_port,
    password="your_password"
)

# Example usage:
key_name = "my_json_key"
json_path = "$.some.object"

object_keys = redis_client.json().objkeys(key_name, json_path)
print(f"Keys of the object at path '{json_path}': {object_keys}")

```

--------------------------------

### Retrieve TTL for Hash Fields in Python

Source: https://upstash.com/docs/redis/sdks/py/commands/hash/httl

Demonstrates how to use the HTTL command in Python to get the remaining time-to-live for fields in a Redis hash. This requires a Redis client library and assumes the hash and fields have been previously set and an expiration time has been applied.

```python
redis.hset(hash_name, field, value)
redis.hexpire(hash_name, field, 10)

assert redis.httl(hash_name, field) == [9]
```

--------------------------------

### Get JSON Value with Python

Source: https://upstash.com/docs/redis/sdks/py/commands/json/get

This snippet demonstrates how to retrieve a JSON value from Upstash Redis using the `redis.json.get` method in Python. It requires the key of the JSON entry and the path to the desired value. The response will be the value at the specified path or null if it doesn't exist.

```python
value = redis.json.get("key", "$.path.to.somewhere")
```

--------------------------------

### Remove Members from Redis Set (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/set/srem

Demonstrates how to add members to a set and then remove specific members using the SREM command in TypeScript. The example shows the usage with the Upstash Redis client and logs the number of members removed.

```typescript
await redis.sadd("set", "a", "b", "c"); 
const removed = await redis.srem("set", "a", "b", "d");
console.log(removed); // 2
```

--------------------------------

### Python: Move Member Between Redis Sets with SMOVE

Source: https://upstash.com/docs/redis/sdks/py/commands/set/smove

This Python example demonstrates how to use the SMOVE command to move a member from a source set to a destination set in Upstash Redis. It first adds members to both sets and then uses smove to transfer a member, verifying the contents of both sets afterward. This operation is atomic and efficient for set manipulation.

```python
redis.sadd("src", "one", "two", "three")

redis.sadd("dest", "four")

assert redis.smove("src", "dest", "three") == True

assert redis.smembers("source") == {"one", "two"}

assert redis.smembers("destination") == {"three", "four"}
```

--------------------------------

### Increment Key Value with Upstash Redis (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/string/incr

Demonstrates how to use the INCR command to increment a key's value in Upstash Redis. This example first sets an initial value for the key and then uses INCR to increment it. The expected output is the new value after the increment.

```typescript
await redis.set("key", 6);
await redis.incr("key");
// returns 7
```

--------------------------------

### Database Configurations

Source: https://upstash.com/docs/redis/integrations/ratelimit/strapi/configurations

Configure the connection details for Upstash Redis.

```APIDOC
## Database Configurations

### Description
Configure the connection parameters for Upstash Redis, including authentication token, URL, and key prefix.

### Parameters
#### Request Body
- **token** (string) - Required - The token to authenticate with the Upstash Redis REST API. Found in Upstash Console as `UPSTASH_REDIS_REST_TOKEN`.
- **url** (string) - Required - The URL for the Upstash Redis REST API. Found in Upstash Console as `UPSTASH_REDIS_REST_URL`.
- **prefix** (string) - Optional - Default: `@strapi` - The prefix for rate limit keys. Used to store rate limit data in Redis. Example: `@strapi:<method>:<route>:<identifier>`.
- **analytics** (boolean) - Optional - Default: `false` - Enable analytics for rate limiting. When enabled, provides insights in Upstash Console.

### Request Example
```json
{
  "token": "YOUR_UPSTASH_TOKEN",
  "url": "https://your-redis-instance.upstash.io",
  "prefix": "@my-app",
  "analytics": true
}
```

### Response
#### Success Response (200)
- **message** (string) - Confirmation message.

#### Response Example
```json
{
  "message": "Database configurations updated successfully."
}
```
```

--------------------------------

### Redis ZINTER Intersection with Weights and SUM Aggregation (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/zset/zunion

Shows how to apply weights to sets during intersection using ZINTER in Python. The 'weights' argument multiplies the scores of elements from corresponding sets before aggregation. This example uses 'aggregate="SUM"' and returns the weighted intersection with scores.

```python
redis.zadd("key1", {"a": 1})

redis.zadd("key2", {"a": 1})

result = redis.zunion(["key1", "key2"],
                        withscores=True,
                        aggregate="SUM",
                        weights=[2, 3])

assert result == [("a", 5)]
```

--------------------------------

### Retrieve Latency Histogram via cURL

Source: https://upstash.com/docs/redis/tutorials/histogram

Retrieves the histogram of recorded latency metrics for a specific test name via a GET request to the API endpoint. The 'name' query parameter specifies which test's data to fetch.

```shell
curl https://v7xx4aa2ib.execute-api.us-east-1.amazonaws.com/get?name=perf-test-1
```

--------------------------------

### Deploy Serverless Service

Source: https://upstash.com/docs/redis/tutorials/rate-limiting

Deploys the configured Serverless Framework application to AWS. This command packages the function code, infrastructure, and configurations, making the service live.

```shell
serverless deploy
```

--------------------------------

### Get Field TTL in Milliseconds (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/hash/hpttl

This Python snippet demonstrates how to use the HPTTL command to retrieve the remaining time-to-live in milliseconds for a specific field within a Redis hash. It assumes the field and hash have already been set and an expiration has been applied.

```Python
redis.hset(hash_name, field, value)
redis.hpexpire(hash_name, field, 1000)

assert redis.hpttl(hash_name, field) == [950]
```

--------------------------------

### HSCAN with Count Option in TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/hash/hscan

Shows how to limit the number of fields returned in a single HSCAN call using the 'count' option. This example sets hash fields and then performs an HSCAN, requesting a maximum of 2 fields per call.

```typescript
await redis.hset("key", {
    id: 1,
    username: "chronark",
    name: "andreas",
  });
  const [newCursor, fields] = await redis.hscan("key", 0, { count: 2 });
  console.log(fields); // ["id", 1, "name", "andreas", "username", "chronark"]
```

--------------------------------

### Configure Environment Variables (.env)

Source: https://upstash.com/docs/redis/tutorials/using_serverless_framework

Sets up environment variables required for connecting to Upstash Redis. These variables, `UPSTASH_REDIS_REST_URL` and `UPSTASH_REDIS_REST_TOKEN`, are crucial for authentication and connection.

```shell
UPSTASH_REDIS_REST_URL=<YOUR_URL>
UPSTASH_REDIS_REST_TOKEN=<YOUR_TOKEN>

```

--------------------------------

### Set Key Expiry with Seconds and Timedelta in Python

Source: https://upstash.com/docs/redis/sdks/py/commands/generic/expire

Demonstrates how to set an expiry time for a Redis key using the EXPIRE command. It shows examples using both integer seconds and datetime.timedelta objects for the timeout duration. After the specified time, the key is automatically deleted.

```python
import redis
import datetime
import time

# Assuming redis is an instance of redis.Redis
redis = redis.Redis(host='YOUR_HOST', port=6379, password='YOUR_PASSWORD')

# With seconds
redis.set("mykey", "Hello")
redis.expire("mykey", 5)

assert redis.get("mykey") == "Hello"

time.sleep(5)

assert redis.get("mykey") is None

# With a timedelta
redis.set("mykey", "Hello")
redis.expire("mykey", datetime.timedelta(seconds=5))
```

--------------------------------

### SQL Rule for MQTT Data Extraction

Source: https://upstash.com/docs/redis/howto/emqxintegration

This SQL query extracts timestamp, client ID, temperature, and humidity from MQTT messages published to the 'temp_hum/emqx' topic. It prepares the data for storage in Upstash Redis.

```sql
SELECT
timestamp as up_timestamp,
clientid as client_id,
payload.temp as temp,
payload.hum as hum
FROM
"temp_hum/emqx"
```

--------------------------------

### Add Members to Redis Set using SADD (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/set/sadd

Demonstrates how to add one or more members to a Redis set using the SADD command with the Upstash Redis client in TypeScript. It shows examples of adding new members and attempting to add existing members.

```typescript
await redis.sadd("key", "a", "b", "c"); 

await redis.sadd("key", "a", "b");
```

--------------------------------

### Sliding Window Rate Limiter (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ratelimit-ts/algorithms

Implements the Sliding Window rate limiting algorithm for Upstash Redis. This algorithm provides a more accurate rate limit by using a rolling window, though it is more resource-intensive. Note the warning about potential performance issues with multi-region setups.

```typescript
const ratelimit = new Ratelimit({
  redis: Redis.fromEnv(),
  limiter: Ratelimit.slidingWindow(10, "10 s"),
});
```

```typescript
const ratelimit = new MultiRegionRatelimit({
  redis: [
    new Redis({
      /* auth */
    }),
    new Redis({
      /* auth */
    })
  ],
  limiter: MultiRegionRatelimit.slidingWindow(10, "10 s"),
});
```

--------------------------------

### Node.js Express Session Management with Redis

Source: https://upstash.com/docs/redis/tutorials/cloud_run_sessions

Implements session management for an Express.js application using the `express-session` middleware and `connect-redis` to store session data in Redis. It requires Redis connection details and tracks user views per URL path. This setup is ideal for stateless serverless environments like Google Cloud Run.

```javascript
var express = require("express");
var parseurl = require("parseurl");
var session = require("express-session");
const redis = require("redis");

var RedisStore = require("connect-redis")(session);
var client = redis.createClient({
  // REPLACE HERE
});

var app = express();

app.use(
  session({
    store: new RedisStore({ client: client }),
    secret: "forest squirrel",
    resave: false,
    saveUninitialized: true,
  })
);

app.use(function (req, res, next) {
  if (!req.session.views) {
    req.session.views = {};
  }

  // get the url pathname
  var pathname = parseurl(req).pathname;

  // count the views
  req.session.views[pathname] = (req.session.views[pathname] || 0) + 1;
  next();
});

app.get("/", function (req, res, next) {
  res.send("you viewed this page " + req.session.views["/"] + " times");
});

app.get("/foo", function (req, res, next) {
  res.send("you viewed this page " + req.session.views["/foo"] + " times");
});

app.get("/bar", function (req, res, next) {
  res.send("you viewed this page " + req.session.views["/bar"] + " times");
});

app.listen(8080, function () {
  console.log("Example app listening on port 8080!");
});
```

--------------------------------

### Get String Length with Redis STRLEN in Python

Source: https://upstash.com/docs/redis/sdks/py/commands/string/strlen

Demonstrates how to set a string value in Redis and then use the STRLEN command to retrieve its length. This requires a Redis client library for Python. The command takes the key as input and returns the integer length of the stored string.

```py
redis.set("key", "Hello World")

assert redis.strlen("key") == 11
```

--------------------------------

### Configure Serverless Framework YAML

Source: https://upstash.com/docs/redis/tutorials/serverless_java_redis

Configures the serverless.yml file to define the service name, provider (AWS), runtime (Java 17), package artifact, and the HTTP API event for the 'hello' function.

```yaml
service: counter-api

frameworkVersion: '3'

provider:
  name: aws
  runtime: java17

package:
  artifact: target/hello-dev.jar

functions:
 hello:
   handler: com.serverless.Handler
   events:
     - httpApi:
         path: /hello
         method: get
```

--------------------------------

### Increment Bitfield Values in Python

Source: https://upstash.com/docs/redis/sdks/py/commands/bitmap/bitfield

This example illustrates incrementing values within a Redis bitfield. It sets an empty key and then increments a 4-bit unsigned integer at offset 0 by 16 and another at offset 4 by 1. The command returns the new values after the increments.

```python
redis.set("mykey", "")

# Increment offset 0 by 16, return 
# Increment offset 4 by 1

result = redis.bitfield("mykey") \
    .incr("u4", 0, 16) \
    .incr("u4", 4, 1) \
    .execute()

assert result == [0, 1]
```

--------------------------------

### Append to JSON Array using Python

Source: https://upstash.com/docs/redis/sdks/py/commands/json/arrappend

Appends specified values to a JSON array located at a given path within a Redis key. This function is useful for dynamically growing arrays stored as JSON in Redis. Ensure the 'redis-py' library is installed.

```python
redis.json.arrappend("key", "$.path.to.array", "a")
```

--------------------------------

### Set Multiple Keys If None Exist (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/string/msetnx

Demonstrates how to use the MSETNX command in Python to set multiple keys and their values at once, but only if none of the specified keys already exist in the Redis instance. This is useful for ensuring atomic updates or initializations. The input is a dictionary of key-value pairs, and the output is a boolean indicating success (all keys set) or failure (at least one key already existed).

```python
redis.msetnx({
    key1: 1,
    key2: "hello",
    key3: { a: 1, b: "hello" },
})
```

--------------------------------

### Retrieve All Hash Fields with HGETALL in TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/hash/hgetall

This snippet demonstrates how to use the HGETALL command with Upstash Redis in a TypeScript environment. It first sets multiple fields in a hash using HSET and then retrieves all of them using HGETALL. The expected output is a JavaScript object containing the hash's fields and values. Ensure you have the Upstash Redis client library installed and configured.

```typescript
await redis.hset("key", {
  field1: "value1",
  field2: "value2",
  });
const hash = await redis.hgetall("key");
console.log(hash); // { field1: "value1", field2: "value2" }
```

--------------------------------

### Decrement Redis Key Value with DECRBY (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/string/decrby

Demonstrates how to use the DECRBY command with Upstash Redis to decrement a key's integer value. This example first sets an initial value and then decrements it. It assumes you have a Redis client instance named 'redis'.

```typescript
await redis.set("key", 6);
await redis.decrby("key", 4);
// returns 2
```

--------------------------------

### Python Redis ZINTER Intersection with Scores and Aggregation

Source: https://upstash.com/docs/redis/sdks/py/commands/zset/zinter

Shows how to perform an intersection with scores and apply a SUM aggregation function using ZINTER in Python. This example adds overlapping elements with different scores to two sets and calculates the sum of their scores in the intersection.

```python
redis.zadd("key1", {"a": 1, "b": 2, "c": 3})

redis.zadd("key2", {"a": 3, "b": 4, "c": 5})

result = redis.zinter(["key1", "key2"], withscores=True, aggregate="SUM")

assert result == [("a", 4), ("b", 6), ("c", 8)]
```

--------------------------------

### Configure Environment Variables for Upstash Redis

Source: https://upstash.com/docs/redis/tutorials/nuxtjs_with_redis

Steps to set up environment variables for connecting to an Upstash Redis database. This involves copying a template file and populating it with credentials obtained from the Upstash console.

```shell
cp .env.example .env
UPSTASH_REDIS_REST_URL=""
UPSTASH_REDIS_REST_TOKEN=""
```

```shell
.env
KV_REST_API_URL=<YOUR_URL>
KV_REST_API_TOKEN=<YOUR_TOKEN>
```

--------------------------------

### Get Multiple Random Fields from Hash (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/hash/hrandfield

This snippet shows how to fetch multiple random fields from a Redis hash using the Upstash Python SDK. The 'count' argument specifies the number of fields to return. The order of fields in the response is not guaranteed.

```python
redis.hset("myhash", values={
    "field1": "Hello",
    "field2": "World"
})

assert redis.hrandfield("myhash", count=2) in [
    ["field1", "field2"],
    ["field2", "field1"]
]
```

--------------------------------

### Pop Element from Redis JSON Array (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/json/arrpop

Removes and returns an element from a JSON array stored in Redis using the JSON.ARRPOP command. This example demonstrates popping the last element by default, and optionally popping the first element by specifying an index of 0.

```python
element = redis.json.arrpop("key", "$.path.to.array")
```

```python
firstElement = redis.json.arrpop("key", "$.path.to.array", 0)
```

--------------------------------

### Retrieve Multiple Fields from Redis Hash (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/hash/hmget

This TypeScript example demonstrates how to use the HMGET command with Upstash Redis to retrieve specific fields from a hash. It first sets some fields using HSET and then fetches 'username' and 'name'. The output is an object containing the requested field-value pairs.

```typescript
await redis.hset("key", {
  id: 1,
  username: "chronark",
  name: "andreas"
  });
const fields = await redis.hmget("key", "username", "name");
console.log(fields); // { username: "chronark", name: "andreas" }
```

--------------------------------

### Configure Environment Variables for Upstash Redis

Source: https://upstash.com/docs/redis/quickstarts/koyeb

These bash commands set environment variables for Upstash Redis connection details. `UPSTASH_REDIS_REST_URL` and `UPSTASH_REDIS_REST_TOKEN` are required by the application to connect to the Redis instance. These should be exported in the terminal before running the application.

```bash
export UPSTASH_REDIS_REST_URL="<YOUR_UPSTASH_REDIS_REST_URL>"
export UPSTASH_REDIS_REST_TOKEN="<YOUR_UPSTASH_REDIS_REST_TOKEN>"
```

--------------------------------

### Increment Counter using Redis in Next.js API

Source: https://upstash.com/docs/redis/quickstarts/nextjs-app-router

This TypeScript API route uses the Upstash Redis client to increment an integer value named 'count' every time the API is called. It returns an 'OK' response upon successful execution. This is useful for tracking simple metrics or counters.

```typescript
import { redis } from "@/lib/redis"

export const POST = async () => {
  await redis.incr("count")

  return new Response("OK")
}
```

--------------------------------

### Connect to Upstash Redis using Environment Variables (TypeScript)

Source: https://upstash.com/docs/redis/howto/vercelintegration

Connect to Upstash Redis by initializing the Redis client using environment variables provided by Vercel. This snippet shows how to set a key, retrieve it, and return the value in a Next.js API route.

```typescript
import { Redis } from "@upstash/redis";
import { type NextRequest, NextResponse } from "next/server";

const redis = Redis.fromEnv();

export const POST = async (request: NextRequest) => {
  await redis.set("foo", "bar");
  const bar = await redis.get("foo");
  return NextResponse.json({
    body: `foo: ${bar}`,
  });
}
```

--------------------------------

### Set Key Expiration with EXPIREAT in Python

Source: https://upstash.com/docs/redis/sdks/py/commands/generic/expireat

Demonstrates how to use the `expireat` command in Python to set a timeout for a Redis key. This can be done using a `datetime.datetime` object or a Unix timestamp. The `set` command is used to initially store the key-value pair. Ensure you have the `redis` and `datetime` libraries installed.

```python
import redis
import datetime
import time

redis_client = redis.Redis(host='YOUR_REDIS_HOST', port=6379, db=0, password='YOUR_REDIS_PASSWORD')

# Example with a datetime object
redis_client.set("mykey", "Hello")
expiry_time_dt = datetime.datetime.now() + datetime.timedelta(seconds=5)
redis_client.expireat("mykey", expiry_time_dt)
print(f"Key 'mykey' set with expiration at {expiry_time_dt}")

# Example with a unix timestamp
redis_client.set("anotherkey", "World")
expiry_time_ts = int(time.time()) + 10
redis_client.expireat("anotherkey", expiry_time_ts)
print(f"Key 'anotherkey' set with expiration at Unix timestamp {expiry_time_ts}")
```

--------------------------------

### Initialize CDK Project with TypeScript

Source: https://upstash.com/docs/redis/quickstarts/aws-lambda

Initializes a new AWS CDK project with TypeScript as the project language. This command sets up the basic structure and configuration files required for a CDK application.

```shell
mkdir counter-cdk && cd counter-cdk
cdk init app --language typescript
```

--------------------------------

### Get Hash Field Expiration Time in Milliseconds - Python

Source: https://upstash.com/docs/redis/sdks/py/commands/hash/hpexpiretime

This Python snippet demonstrates how to set a hash field with an expiration and then retrieve its expiration time using HPEXPIRETIME. It assumes a Redis connection is established and uses the Upstash Redis client library.

```python
import redis
import time

# Assuming 'redis' is an initialized Upstash Redis client instance
hash_name = "myhash"
field = "myfield"
value = "myvalue"

# Set the field in the hash
redis.hset(hash_name, field, value)

# Set an expiration time for the field (1 second from now)
expiration_ms = int(time.time() * 1000) + 1000
redis.hpexpireat(hash_name, field, expiration_ms)

# Retrieve the expiration time of the field
expiration_time = redis.hpexpiretime(hash_name, field)

# Assert that the retrieved expiration time is close to the set time (allowing for slight differences)
# Note: The exact value might vary slightly due to timing. For precise testing, comparing within a range or checking the return type might be more robust.
print(f"Expiration time for field '{field}': {expiration_time}")
assert isinstance(expiration_time, list) and len(expiration_time) == 1 and expiration_time[0] > 0
```

--------------------------------

### AWS CDK Stack: Lambda Function with Upstash Redis Environment

Source: https://upstash.com/docs/redis/quickstarts/python-aws-lambda

Configures an AWS Lambda function using AWS CDK in TypeScript. It specifies the Python runtime, handler, and environment variables for Upstash Redis connection. Includes bundling instructions to install Python dependencies.

```typescript
import * as cdk from 'aws-cdk-lib';
import { Construct } from 'constructs';
import * as lambda from 'aws-cdk-lib/aws-lambda';
import * as path from 'path';

export class CounterCdkStack extends cdk.Stack {
  constructor(scope: Construct, id: string, props?: cdk.StackProps) {
    super(scope, id, props);

    const counterFunction = new lambda.Function(this, 'CounterFunction', {
      code: lambda.Code.fromAsset(path.join(__dirname, 'api'), {
        bundling: {
          image: lambda.Runtime.PYTHON_3_9.bundlingImage,
          command: [
            'bash', '-c',
            'pip install -r requirements.txt -t /asset-output && cp -au . /asset-output'
          ],
        },
      }),
      runtime: lambda.Runtime.PYTHON_3_9,
      handler: 'index.handler',
      environment: {
        UPSTASH_REDIS_REST_URL: process.env.UPSTASH_REDIS_REST_URL || '',
        UPSTASH_REDIS_REST_TOKEN: process.env.UPSTASH_REDIS_REST_TOKEN || '',
      },
    });

    const counterFunctionUrl = counterFunction.addFunctionUrl({
      authType: lambda.FunctionUrlAuthType.NONE,
    });

    new cdk.CfnOutput(this, "counterFunctionUrlOutput", {
      value: counterFunctionUrl.url,
    })
  }
}
```

--------------------------------

### Configure Serverless Service (serverless.yml)

Source: https://upstash.com/docs/redis/tutorials/using_serverless_framework

Defines the Serverless Framework service configuration. It specifies the AWS provider, runtime, environment variables for Upstash Redis, and the HTTP-triggered Lambda function.

```yaml
service: counter-serverless

provider:
  name: aws
  runtime: nodejs20.x
  environment:
    UPSTASH_REDIS_REST_URL: ${env:UPSTASH_REDIS_REST_URL}
    UPSTASH_REDIS_REST_TOKEN: ${env:UPSTASH_REDIS_REST_TOKEN}

functions:
  counter:
    handler: handler.counter
    events:
      - httpApi:
          path: /
          method: get

```

--------------------------------

### Disable base64 response encoding in Upstash Redis

Source: https://upstash.com/docs/redis/sdks/ts/troubleshooting

To prevent Upstash Redis from returning responses as base64 encoded strings, disable the `responseEncoding` option by setting it to `false` during client initialization. This is useful if the default encoding causes issues with deserialization.

```typescript
const redis = new Redis({
  // ...
  responseEncoding: false,
});
```

--------------------------------

### Write Multiple Fields to a Hash using Python

Source: https://upstash.com/docs/redis/sdks/py/commands/hash/hmset

This snippet demonstrates how to use the `hset` command (equivalent to HMSET for multiple fields) in Python to set multiple fields and their values within a Redis hash. It expects the hash key and a dictionary of fields as input, returning an integer representing the number of fields successfully added. Ensure the redis-py library is installed.

```python
import redis

redis_client = redis.Redis(host="YOUR_REDIS_HOST", port=6379, password="YOUR_REDIS_PASSWORD")

# Set multiple fields
hash_key = "myhash"
fields_to_set = {
  "field1": "Hello",
  "field2": "World"
}

result = redis_client.hset(hash_key, mapping=fields_to_set)

print(f"Number of fields added: {result}")
# Example assertion:
# assert result == 2
```

--------------------------------

### Remove and Return Array Element with JSON.ARRPOP (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/json/arrpop

This example demonstrates how to use the JSON.ARRPOP command to remove and return an element from a JSON array. It utilizes the Upstash Redis client in TypeScript. The function takes a key and an optional path to the array, defaulting to the last element if no index is provided.

```typescript
const element = await redis.json.arrpop("key", "$.path.to.array");
```

```typescript
const firstElement = await redis.json.arrpop("key", "$.path.to.array", 0);
```

--------------------------------

### Node.js Redis Client Initialization and Query Handler

Source: https://upstash.com/docs/redis/tutorials/auto_complete_with_serverless_redis

Initializes an ioredis client using the REDIS_URL from environment variables and defines an AWS Lambda handler function to process autocomplete queries. It retrieves search terms from query parameters, uses Redis ZRANK and ZRANGE to find matching suggestions from a sorted set, and returns results with CORS headers.

```javascript
var Redis = require("ioredis");
if (typeof client === "undefined") {
  var client = new Redis(process.env.REDIS_URL);
}
const headers = {
  "Access-Control-Allow-Origin": "*",
  "Access-Control-Allow-Credentials": true,
};

module.exports.query = async (event, context, callback) => {
  if (!event.queryStringParameters || !event.queryStringParameters.term) {
    return {
      statusCode: 400,
      headers: headers,
      body: JSON.stringify({
        message: "Invalid parameters. Term needed as query param.",
      }),
    };
  }
  let term = event.queryStringParameters.term.toUpperCase();
  let res = [];
  let rank = await client.zrank("terms", term);
  if (rank != null) {
    let temp = await client.zrange("terms", rank, rank + 100);
    for (const el of temp) {
      if (!el.startsWith(term)) {
        break;
      }
      if (el.endsWith("*")) {
        res.push(el.substring(0, el.length - 1));
      }
    }
  }
  return {
    statusCode: 200,
    headers: headers,
    body: JSON.stringify({
      message: "Query:" + event.queryStringParameters.term,
      result: res,
    }),
  };
};
```

--------------------------------

### Remove Multiple Random Set Members with SPOP in Python

Source: https://upstash.com/docs/redis/sdks/py/commands/set/spop

Illustrates using the `spop` command in Python to remove and return multiple random members from a Redis set by specifying a count. The example adds members and then uses `spop` with a count of 2.

```python
redis.sadd("myset", "one", "two", "three")

assert redis.spop("myset", 2) in {"one", "two", "three"}
```

--------------------------------

### Example Error Message for Max Daily Request Limit

Source: https://upstash.com/docs/redis/troubleshooting/max_daily_request_limit

This snippet shows the typical error message a client receives when the maximum daily request limit for Upstash Redis is exceeded. It highlights the 'ReplyError' and the specific error string.

```text
ReplyError: ERR max daily request limit exceeded
```

--------------------------------

### Increment Sorted Set Member Score with TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/zset/zincrby

Demonstrates how to use the ZINCRBY command with TypeScript to increment a member's score in a sorted set. It assumes a 'redis' client instance is available and shows an example of adding a member first, then incrementing its score.

```typescript
await redis.zadd("key", 1, "member");
const value = await redis.zincrby("key", 2, "member");
console.log(value); // 3
```

--------------------------------

### Seed Database with Sample Data

Source: https://upstash.com/docs/redis/tutorials/laravel_caching

Runs the database seeders defined in your application, populating the database with the sample todo items created by the `DatabaseSeeder`.

```shell
php artisan db:seed
```

--------------------------------

### Initialize Redis Client and Increment Counter

Source: https://upstash.com/docs/redis/quickstarts/ion

Initializes the Upstash Redis client using environment variables and increments a counter on the home page. This demonstrates a basic interaction with the Redis database.

```typescript
import { Redis } from "@upstash/redis";

const redis = Redis.fromEnv();

export default async function Home() {
  const count = await redis.incr("counter");
  return (
    <div className="flex h-screen w-screen items-center justify-center">
      <h1 className="text-4xl font-bold">Counter: {count}</h1>
    </div>
  )
}
```

--------------------------------

### Get Multiple Random Fields from Hash (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/hash/hrandfield

Retrieves a specified number of random fields from a hash key. This overloaded version of HRANDFIELD takes a count argument to determine how many fields to return. The output is an array of strings representing field names.

```typescript
await redis.hset("key", {
  id: 1,
  username: "chronark",
  name: "andreas",
});
const randomFields = await redis.hrandfield("key", 2);
console.log(randomFields); // ["id", "username"] or any other combination
```

--------------------------------

### Iterate Through Hash Members using Python

Source: https://upstash.com/docs/redis/sdks/py/commands/hash/hscan

This Python code snippet demonstrates how to use the `hscan` command to retrieve all members of a hash. It uses a `while` loop to paginate through the results, starting with a cursor of 0 and continuing until the cursor returns 0, indicating the end of the hash. The `match` parameter can be used to filter field names.

```python
# Get all members of a hash.

cursor = 0
results = []

while True:
    cursor, keys = redis.hscan("myhash", cursor, match="*")

    results.extend(keys)
    if cursor == 0:
        break

```

--------------------------------

### Testing the Producer with Serverless Invoke Local

Source: https://upstash.com/docs/redis/tutorials/job_processing

This shell command demonstrates how to locally invoke a serverless function named 'hello' to test the producer side of the application. It sends a JSON payload containing employee details to the function, which is expected to then add a job to the queue.

```shell
serverless invoke local -f hello -d "{name:'Bill Gates', email:'bill@upstash.com', position:'Developer', date:'20210620'}"
```

--------------------------------

### Elixir Phoenix Controller for Redis Status and Home Page

Source: https://upstash.com/docs/redis/quickstarts/elixir

This Elixir code defines the `PageController` for a Phoenix application. It includes a `Payload` struct for data transfer, a `status` function to test Redis connection using `Redix.command("PING")`, a `home` function for the default page, and a private `render_home` function to render the 'home.html' view. It handles both successful and error responses from Redis.

```elixir
defmodule RedixDemoWeb.PageController do
  use RedixDemoWeb, :controller

  defmodule Payload do
    defstruct text: nil, weather: nil, location: nil
  end

  def status(conn, _params) do
    case Redix.command(:redix, ["PING"])
      {:ok, response} ->
        render_home(conn, %Payload{text: "Redis Connection Status: Success! Response to 'PING': '#{response}'"})
      {:error, response} ->
        render_home(conn, %Payload{text: "Redis Connection Status: Error. Reason: #{response.reason}"})
    end
  end

  def home(conn, _params) do
    render_home(conn, %Payload{text: "Enter a location above to get the weather info!"})
  end

  defp render_home(conn, %Payload{} = payload) do
    render(conn, "home.html", text: payload.text, weather: payload.weather, location: payload.location)
  end
end
```

--------------------------------

### Get Random Field and Value from Hash (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/hash/hrandfield

This snippet illustrates how to retrieve a random field along with its value from a Redis hash using the Upstash Python SDK. The 'withvalues' argument must be set to True, and 'count' can be used to specify the number of field-value pairs.

```python
redis.hset("myhash", values={
    "field1": "Hello",
    "field2": "World"
})

assert redis.hrandfield("myhash", count=1, withvalues=True) in [
    {"field1": "Hello"},
    {"field2": "World"}
]
```

--------------------------------

### Access Koyeb Deployment Logs

Source: https://upstash.com/docs/redis/quickstarts/koyeb

Retrieves build logs for a specific Koyeb service to monitor the deployment process. The command targets the build logs.

```bash
koyeb service logs example-koyeb-upstash/example-koyeb-upstash -t build
```

--------------------------------

### Increment Hash Field by Float (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/hash/hincrbyfloat

This Python example demonstrates how to use the HINCRBYFLOAT command to increment a hash field's value by a float. It first sets an initial value and then asserts that the increment operation results in the expected new value. This operation is atomic and handles potential floating-point inaccuracies.

```python
redis.hset("myhash", "field1", 5.5)

assert redis.hincrbyfloat("myhash", "field1", 10.1) - 15.6 < 0.0001
```

--------------------------------

### Insert Element Before Pivot in Redis List (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/list/linsert

This example demonstrates how to use the LINSERT command to insert a new element ('x') before an existing element ('b') in a Redis list associated with the key 'key'. It assumes the list 'key' already contains elements 'a', 'b', and 'c'. The function returns the new length of the list after insertion, or specific error codes if the pivot is not found or the list does not exist.

```ts
await redis.rpush("key", "a", "b", "c");
await redis.linsert("key", "before", "b", "x");
```

--------------------------------

### Configure Request Timeout in Upstash Redis (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/advanced

This example demonstrates how to set a request timeout for Upstash Redis operations using the `AbortSignal.timeout` method. If a request exceeds the specified duration (in milliseconds), a TimeoutError will be thrown. Error handling for timeouts is also included.

```typescript
try {
  const redis = new Redis({
    url: "<UPSTASH_REDIS_REST_URL>",
    token: "<UPSTASH_REDIS_REST_TOKEN>",
    // set a timeout of 1 second
    signal: () => AbortSignal.timeout(1000),
  });
} catch (error) {
  if (error.name === "TimeoutError") {
    console.error("Request timed out");
  } else {
    console.error("An error occurred:", error);
  }
}
```

--------------------------------

### LPOS Command Documentation

Source: https://upstash.com/docs/redis/sdks/ts/commands/list/lpos

Provides details on how to use the LPOS command to find elements in a Redis list, including options for rank, count, and maxLen.

```APIDOC
## LPOS

### Description
Returns the index of matching elements inside a list.

### Method
GET (or other appropriate method if specific to the client library, e.g., POST for command execution)

### Endpoint
/websites/upstash-redis

### Parameters
#### Query Parameters
- **key** (string) - Required - The key of the list.
- **element** (unknown) - Required - The element to match.
- **rank** (number) - Optional - The rank of the element to match. If specified, the element at the given rank is matched instead of the first element.
- **count** (number) - Optional - The maximum number of elements to match. If specified, an array of elements is returned instead of a single element.
- **maxLen** (number) - Optional - Limit the number of comparisons to perform.

### Request Example
```ts
// Basic usage
await redis.rpush("key", "a", "b", "c"); 
const index = await redis.lpos("key", "b");
console.log(index);

// With rank option
await redis.rpush("key", "a", "b", "c", "b"); 
const indexWithRank = await redis.lpos("key", "b", { rank: 2 });
console.log(indexWithRank);

// With count option
await redis.rpush("key", "a", "b", "b");
const positions = await redis.lpos("key", "b", { count: 2 });
console.log(positions);
```

### Response
#### Success Response (200)
- **(number | number[])** - Required - The index of the matching element or an array of indexes if `opts.count` is specified.
```

--------------------------------

### Get Set Difference with Scores (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/zset/zdiff

Calculates the difference between two sets stored in Redis, including their associated scores. This function returns tuples of (element, score) for elements present in the first set but not in the second. It's useful when the score associated with each element is relevant.

```python
redis.zadd("key1", {"a": 1, "b": 2, "c": 3})

redis.zadd("key2", {"c": 3, "d": 4, "e": 5})

result = redis.zdiff(["key1", "key2"], withscores=True)

assert result == [("a", 1), ("b", 2)]
```

--------------------------------

### Decrement Key Value in Python with Upstash Redis

Source: https://upstash.com/docs/redis/sdks/py/commands/string/decr

This Python snippet demonstrates how to use the DECR command with Upstash Redis. It first sets a key to a specific integer value and then decrements it, asserting the expected result. Ensure the 'redis' library is installed and configured for Upstash.

```python
redis.set("key", 6)

assert redis.decr("key") == 5
```

--------------------------------

### Configure Project Dependencies

Source: https://upstash.com/docs/redis/tutorials/rate-limiting

Defines the project's dependencies in `package.json`, including `@upstash/ratelimit` for rate limiting logic and `@upstash/redis` for Redis integration.

```json
{
    "dependencies": {
      "@upstash/ratelimit": "latest",
      "@upstash/redis": "latest"
    }
  }
```

--------------------------------

### Configure Upstash Redis Environment Variables

Source: https://upstash.com/docs/redis/tutorials/nextjs_with_redis

Sets up environment variables for connecting to your Upstash Redis instance. Ensure you replace placeholders with your actual URL and token.

```env
UPSTASH_REDIS_REST_URL=<YOUR_URL>
UPSTASH_REDIS_REST_TOKEN=<YOUR_TOKEN>
```

```env
KV_REST_API_URL=<YOUR_URL>
KV_REST_API_TOKEN=<YOUR_TOKEN>
```

--------------------------------

### Get JSON Object Keys with Upstash Redis (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/json/objkeys

This snippet demonstrates how to use the JSON.OBJKEYS command with Upstash Redis in TypeScript. It retrieves the keys of a JSON object stored at a given key and path. This function requires the 'redis' client instance and expects a string key and path as input, returning a 2D string array of the object's keys.

```typescript
const keys = await redis.json.objkeys("key", "$.path");
```

--------------------------------

### Get JSON Array Length with TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/json/arrlen

Reports the length of the JSON array at a specified path within a key using the Upstash Redis client in TypeScript. This function requires the redis client to be initialized and takes the key and path as string arguments, returning an integer array representing the length.

```typescript
const length = await redis.json.arrlen("key", "$.path.to.array");
```

--------------------------------

### Append Value to JSON Array in Redis (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/json/arrappend

Appends a value to an array at a specified path within a JSON document stored in Redis using the JSON.ARRAPPEND command. This example demonstrates the basic usage with a string value. Ensure you have the Upstash Redis client initialized.

```typescript
await redis.json.arrappend("key", "$.path.to.array", "a");
```

--------------------------------

### Enable Auto-Pipelining with Redis Client

Source: https://upstash.com/docs/redis/sdks/ts/pipelining/auto-pipeline

Demonstrates how to enable auto-pipelining when creating a Redis client using `Redis.fromEnv` or by directly providing URL and token. Auto-pipelining batches commands sent to Redis.

```typescript
import { Redis } from "@upstash/redis";

const redis = Redis.fromEnv({
  latencyLogging: false,
  enableAutoPipelining: true
});
```

```typescript
import { Redis } from "@upstash/redis";

const redis = new Redis({
  url: <UPSTASH_REDIS_REST_URL>,
  token: <UPSTASH_REDIS_REST_TOKEN>,
  enableAutoPipelining: true
})
```

--------------------------------

### Increment Hash Field Value with HINCRBY (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/hash/hincrby

Demonstrates how to use the HINCRBY command to increment a hash field's value in Upstash Redis. This example first sets an initial value for a field using HSET and then uses HINCRBY to increment it, logging the result. Ensure you have the Upstash Redis client initialized.

```typescript
await redis.hset("key", {
  field: 20,
});
const after = await redis.hincrby("key", "field", 2);
console.log(after); // 22
```

--------------------------------

### Get Hash Field Expiration Time - Python

Source: https://upstash.com/docs/redis/sdks/py/commands/hash/hexpiretime

This Python code snippet demonstrates how to set a field in a Redis hash, assign an expiration time to it, and then retrieve that expiration time using the HEXPIRETIME command. It asserts that the retrieved expiration time matches the expected value.

```python
redis.hset(hash_name, field, value)
redis.hexpireat(hash_name, field, int(time.time()) + 10)

assert redis.hexpiretime(hash_name, field) == [1697059200]
```

--------------------------------

### Decrement Redis Key Value with Python (DECRBY)

Source: https://upstash.com/docs/redis/sdks/py/commands/string/decrby

This Python code snippet demonstrates how to use the DECRBY command to decrement a Redis key's value. It first sets an initial value for the key and then decrements it by a specified amount, asserting the final value. Ensure you have the Upstash Redis client library installed.

```python
redis.set("key", 6)

assert redis.decrby("key", 4) == 2
```

--------------------------------

### Check if Hash Field Exists in Upstash Redis (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/hash/hexists

This TypeScript example demonstrates how to use the HEXISTS command with Upstash Redis. It first sets a field in a hash using HSET and then checks for its existence using HEXISTS. The result, 1 or 0, is logged to the console.

```typescript
await redis.hset("key", "field", "value");
const exists = await redis.hexists("key", "field");

console.log(exists); // 1
```

--------------------------------

### Create Serverless Project

Source: https://upstash.com/docs/redis/tutorials/rate-limiting

Scaffolds a new Serverless Framework project for AWS Lambda using the Node.js HTTP API template. It prompts for project and app names and configures the initial structure.

```shell
serverless

# Follow prompts for template, project name, and app name.
```

--------------------------------

### Find JSON Array Index - Python

Source: https://upstash.com/docs/redis/sdks/py/commands/json/arrindex

This Python snippet demonstrates how to use the `redis.json.arrindex` command to find the first occurrence of a value within a JSON array. It requires the `redis` library to be installed and configured to connect to an Upstash Redis instance. The function returns the index of the value or -1 if not found.

```python
import redis

r = redis.Redis(host='YOUR_UPSTASH_REDIS_HOST', port=YOUR_UPSTASH_REDIS_PORT, password='YOUR_UPSTASH_REDIS_PASSWORD')

# Example: Find the index of 'a' in the array at '$.path.to.array'
# Assuming 'key' holds a JSON document with an array at '$.path.to.array'
# For instance: '{"path": {"to": {"array": ["a", "b", "c", "a"]}}}'
index = r.json().arrindex('key', '$.path.to.array', 'a')
print(f"Index of 'a': {index}")

# Example: Search within a range (e.g., from index 1 to 3)
index_ranged = r.json().arrindex('key', '$.path.to.array', 'a', start=1, stop=3)
print(f"Index of 'a' between 1 and 3: {index_ranged}")
```

--------------------------------

### HTML Chat Interface and Client-Side JavaScript

Source: https://upstash.com/docs/redis/tutorials/python_realtime_chat

Provides the HTML structure for a real-time chat interface, including basic CSS for styling. It also contains client-side JavaScript to establish a WebSocket connection, manage user sessions, display messages, and send new messages to the server.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Real-Time Chat</title>
    <script src="https://cdn.socket.io/4.5.4/socket.io.min.js"></script>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            background-color: #f4f6f9;
        }

        #chat-container {
            width: 90%;
            max-width: 600px;
            height: 70%;
            border: 1px solid #ddd;
            border-radius: 10px;
            background-color: #fff;
            display: flex;
            flex-direction: column;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        #chat-box {
            flex: 1;
            overflow-y: auto;
            padding: 15px;
            border-bottom: 1px solid #ddd;
            scrollbar-width: thin;
            scrollbar-color: #ccc #f4f6f9;
        }

        #chat-box::-webkit-scrollbar {
            width: 8px;
        }

        #chat-box::-webkit-scrollbar-thumb {
            background: #ccc;
            border-radius: 5px;
        }

        .message {
            margin: 10px 0;
            padding: 10px 15px;
            border-radius: 15px;
            max-width: 70%;
            word-wrap: break-word;
        }

        .message.sent {
            align-self: flex-end;
            background-color: #007BFF;
            color: white;
        }

        .message.received {
            align-self: flex-start;
            background-color: #f1f1f1;
            color: black;
        }

        #input-container {
            display: flex;
            padding: 10px;
            gap: 10px;
            background-color: #f4f6f9;
            border-radius: 0 0 10px 10px;
        }

        #message-input {
            flex: 1;
            padding: 10px;
            font-size: 16px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        #send-button {
            padding: 10px 20px;
            font-size: 16px;
            border: none;
            border-radius: 5px;
            background-color: #007BFF;
            color: white;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        #send-button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <div id="chat-container">
        <div id="chat-box"></div>
        <div id="input-container">
            <input id="message-input" type="text" placeholder="Type your message...">
            <button id="send-button">Send</button>
        </div>
    </div>

    <script>
        const socket = io();

        const chatBox = document.getElementById("chat-box");
        const messageInput = document.getElementById("message-input");
        const sendButton = document.getElementById("send-button");

        // Generate or retrieve a random username for this tab
        function getUsername() {
            let username = sessionStorage.getItem("username");
            if (!username) {
                username = "User" + Math.floor(Math.random() * 1000); // Temporary random username
                sessionStorage.setItem("username", username);
            }
            return username;
        }

        const username = getUsername();

        // Append message to chat box
        function addMessage(message, type = "received") {
            const messageElement = document.createElement("div");
            messageElement.textContent = message;
            messageElement.classList.add("message", type);
            chatBox.appendChild(messageElement);
            chatBox.scrollTop = chatBox.scrollHeight;
        }

        // Receive messages from server
        socket.on("message", (data) => {
            addMessage(`${data.user}: ${data.message}`, "received");
        });

        // Send message to server
        sendButton.addEventListener("click", () => {
            const message = messageInput.value.trim();
            if (message) {
                socket.emit("message", { user: username, message: message });
                addMessage(`${username}: ${message}`, "sent");
                messageInput.value = "";
            }
        });

        messageInput.addEventListener("keypress", (event) => {
            if (event.key === "Enter") {
                sendButton.click();
            }
        });
    </script>
</body>
</html>

```

--------------------------------

### Trim JSON Array with TypeScript - Upstash Redis

Source: https://upstash.com/docs/redis/sdks/ts/commands/json/arrtrim

Demonstrates how to use the JSON.ARRTRIM command to trim a JSON array stored in Redis. This function requires the Upstash Redis client and takes the key, path to the array, start index, and stop index as arguments. It returns the new length of the array.

```typescript
const length = await redis.json.arrtrim("key", "$.path.to.array", 2, 10);

```

--------------------------------

### Get Multiple Random Set Members (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/set/srandmember

Retrieves a specified number of random members from a set in Upstash Redis. This is useful when you need a collection of random, unique elements from a set. The `count` argument determines how many members are returned. It requires the Upstash Redis client to be initialized.

```typescript
await redis.sadd("set", "a", "b", "c"); 
const members = await redis.srandmember("set", 2);
console.log(members); // ["a", "b"]
```

--------------------------------

### Avoiding Frequent Awaits with Promise.all for Auto-Pipelining

Source: https://upstash.com/docs/redis/sdks/ts/pipelining/auto-pipeline

Shows the difference between awaiting individual commands and using `Promise.all` with auto-pipelining. Awaiting each command triggers a separate pipeline call. Using `Promise.all` ensures commands are batched into a single `PIPELINE` command for better efficiency.

```typescript
// makes a single PIPELINE call:
const [ foo, bar ] = await Promise.all([
  redis.get("foo"),
  redis.get("bar")
])
```

--------------------------------

### Get Random Fields with Values from Hash (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/hash/hrandfield

Retrieves a specified number of random fields and their corresponding values from a hash key. By setting the third argument to 'true', the HRANDFIELD command returns an object containing both field names and their values. This is useful for inspecting random data entries.

```typescript
await redis.hset("key", {
  id: 1,
  username: "chronark",
  name: "andreas",
});
const randomFields = await redis.hrandfield("key", 2, true);
console.log(randomFields); // { id: "1", username: "chronark" } or any other combination
```

--------------------------------

### Get Random Set Member (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/set/srandmember

Retrieves a single random member from a specified set in Upstash Redis. This function is useful for selecting a single random element without needing to know the set's contents beforehand. It requires the Upstash Redis client to be initialized.

```typescript
await redis.sadd("set", "a", "b", "c"); 
const member = await redis.srandmember("set");
console.log(member); // "a"
```

--------------------------------

### Initialize Azure Functions Project (TypeScript)

Source: https://upstash.com/docs/redis/quickstarts/azure-functions

Initializes a new Azure Functions project with TypeScript as the runtime. This command sets up the basic project structure and configuration files required for developing Azure Functions.

```shell
func init --typescript
```

--------------------------------

### Set Upstash Redis Environment Variables

Source: https://upstash.com/docs/redis/tutorials/python_url_shortener

Sets environment variables for Upstash Redis connection details. These variables, UPSTASH_REDIS_REST_URL and UPSTASH_REST_TOKEN, are required for the Python client to authenticate and connect to your Redis database. These can be set directly in the shell or loaded from a .env file.

```shell
export UPSTASH_REDIS_REST_URL=<YOUR_URL>
export UPSTASH_REDIS_REST_TOKEN=<YOUR_TOKEN>
```

```text
UPSTASH_REDIS_REST_URL=<YOUR_URL>
UPSTASH_REDIS_REST_TOKEN=<YOUR_TOKEN>
```

--------------------------------

### Count Elements in Sorted Set by Score (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/zset/zcount

Demonstrates how to use the ZCOUNT command to count elements in a Redis sorted set within a given score range. This example first adds elements to a sorted set using ZADD and then uses ZCOUNT to count elements with scores greater than 1. It requires the Upstash Redis client library.

```typescript
await redis.zadd("key", 
    { score: 1, member: "one"},
    { score: 2, member: "two" },
);
const elements = await redis.zcount("key", "(1", "+inf");
console.log(elements); // 1
```

--------------------------------

### Deploy to Google Cloud Run

Source: https://upstash.com/docs/redis/tutorials/cloud_run_sessions

This command deploys your containerized application to Google Cloud Run as a managed service. It specifies the image to use, the platform, the region, and allows unauthenticated access to the service. The output includes the service URL upon successful deployment.

```bash
gcloud run deploy cloud-run-sessions \
  --image gcr.io/cloud-run-sessions/main:v0.1 \
  --platform managed \
  --region us-central1 \
  --allow-unauthenticated
```

--------------------------------

### Count Elements in Sorted Set by Score (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/zset/zcount

This Python snippet demonstrates how to use the ZCOUNT command with Upstash Redis. It first adds elements to a sorted set using ZADD and then counts the elements within a specified score range. The example shows how to use exclusive bounds for the minimum score and an infinite upper bound.

```python
redis.zadd("key", 
    { score: 1, member: "one"},
    { score: 2, member: "two" },
)
elements = redis.zcount("key", "(1", "+inf")
print(elements); # 1
```

--------------------------------

### JavaScript: Handle User Messages and Enter Keypress in Chat

Source: https://upstash.com/docs/redis/tutorials/python_realtime_chat

This JavaScript code handles sending messages from the user interface and also implements a feature to send a message by pressing the Enter key. It interacts with a socket for real-time communication.

```javascript
                addMessage(`You: ${message}`, "sent");
                socket.emit("message", { user: username, message });
                messageInput.value = "";
            }
        });

        // Optional: Press Enter to send a message
        messageInput.addEventListener("keypress", (e) => {
            if (e.key === "Enter") {
                sendButton.click();
            }
        });
    </script>
</body>
</html>
```

--------------------------------

### Redis Command for Storing Data

Source: https://upstash.com/docs/redis/howto/emqxintegration

This Bash command, executed via EMQX data integration, stores extracted MQTT data into Upstash Redis using the HMSET command. It uses the client ID as the key and the timestamp, temperature, and humidity as values.

```bash
HMSET ${client_id} ${up_timestamp} ${temp}
```

--------------------------------

### Retrieve large numbers as strings from Upstash Redis

Source: https://upstash.com/docs/redis/sdks/ts/troubleshooting

When storing large numbers that exceed JavaScript's safe integer limit (2^53 - 1), the Upstash Redis client will return them as strings to avoid precision loss. This snippet shows setting a large number and retrieving it, illustrating the string output.

```typescript
await redis.set("key", "101600000000150081467");
const res = await redis("get");

// "101600000000150081467"
```

--------------------------------

### Apply Rate Limit for All Routes (JSON)

Source: https://upstash.com/docs/redis/integrations/ratelimit/strapi/configurations

This configuration applies a fixed-window rate limit to all routes ('*') for specified HTTP methods. It uses the 'Authorization' header to identify unique clients. The limit is set to 10 tokens within a 20-second window.

```json
{
   "strapi-plugin-upstash-ratelimit":{
      "enabled":true,
      "resolve":"./src/plugins/strapi-plugin-upstash-ratelimit",
      "config":{
         "enabled":true,
         "token":"process.env.UPSTASH_REDIS_REST_TOKEN",
         "url":"process.env.UPSTASH_REDIS_REST_URL",
         "strategy":[
            {
               "methods":[
                  "GET",
                  "POST"
               ],
               "path":"*",
               "identifierSource":"header.Authorization",
               "limiter":{
                  "algorithm":"fixed-window",
                  "tokens":10,
                  "window":"20s"
               }
            }
         ],
         "prefix":"@strapi"
      }
   }
}
```

--------------------------------

### Get Hash Field String Length with Upstash Redis (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/hash/hstrlen

Retrieves the string length of a specified field within a hash stored in Upstash Redis. It requires the key of the hash and the name of the field. Returns 0 if the hash or field does not exist, otherwise returns the length of the string value.

```typescript
const length = await redis.hstrlen("key", "field")
```

--------------------------------

### Trim JSON Array using Python and Upstash Redis

Source: https://upstash.com/docs/redis/sdks/py/commands/json/arrtrim

This Python code snippet demonstrates how to use the JSON.ARRTRIM command with Upstash Redis. It trims a JSON array stored at a specified key and path, keeping elements within the given start and stop indices. The function returns the updated length of the array.

```python
length = redis.json.arrtrim("key", "$.path.to.array", 2, 10)
```

--------------------------------

### Get Member Rank in Sorted Set (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/zset/zrank

This Python code snippet demonstrates how to use the ZRANK command with Upstash Redis. It first adds members to a sorted set using ZADD and then uses ZRANK to retrieve the rank of existing and non-existing members, asserting the expected results. This function is useful for understanding the ordered position of elements in a Redis sorted set.

```python
redis.zadd("myset", {"a": 1, "b": 2, "c": 3})

assert redis.zrank("myset", "a") == 0

assert redis.zrank("myset", "d") == None

assert redis.zrank("myset", "b") == 1

assert redis.zrank("myset", "c") == 2
```

--------------------------------

### Redis LPOS Basic Usage

Source: https://upstash.com/docs/redis/sdks/py/commands/list/lpos

Demonstrates the basic usage of the LPOS command to find the index of an element in a Redis list. Assumes a Redis client is initialized.

```python
redis.rpush("key", "a", "b", "c"); 

assert redis.lpos("key", "b") == 1
```

--------------------------------

### Elixir Phoenix Router Configuration

Source: https://upstash.com/docs/redis/quickstarts/elixir

This Elixir code updates the router configuration for a Phoenix application. It defines routes for `/status`, `/`, and `/:text`, mapping them to the `PageController`'s `status` and `home` actions. The `/:text` route allows capturing any text as a parameter.

```elixir
scope "/", RedixDemoWeb do
  pipe_through :browser

  get "/status", PageController, :status

  get "/", PageController, :home
  get "/:text", PageController, :home
end
```

--------------------------------

### Get Hash Field String Length with Python (Upstash Redis)

Source: https://upstash.com/docs/redis/sdks/py/commands/hash/hstrlen

This snippet demonstrates how to use the `hstrlen` command in Python with Upstash Redis to retrieve the string length of a field within a hash. It requires the `redis` library and assumes a Redis connection object is already established. The function takes the key and field as input and returns the length as an integer.

```python
length = redis.hstrlen("key", "field")
```

--------------------------------

### Set Field Expiration in Hash with HPEXPIREAT (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/hash/hpexpireat

This example demonstrates how to use the HPEXPIREAT command to set an expiration time for a field within a Redis hash using Upstash. It first sets a field-value pair using HSET and then uses HPEXPIREAT to set the expiration in milliseconds. The result indicates whether the expiration was successfully set.

```typescript
await redis.hset("my-key", "my-field", "my-value");
const expirationSet = await redis.hpexpireat("my-key", "my-field", Date.now() + 1000);

console.log(expirationSet); // [1]
```

--------------------------------

### Database Seeder for Creating Sample Todos

Source: https://upstash.com/docs/redis/tutorials/laravel_caching

This seeder class utilizes the 'TodoFactory' to create 50 sample 'Todo' records when the database seeding process is run. It populates the database with initial data for the application.

```php
<?php

namespace Database\Seeders;

use App\Models\Todo;
use App\Models\User;
use Illuminate\Database\Seeder;

class DatabaseSeeder extends Seeder
{
    /**
     * Seed the application's database.
     */
    public function run(): void
    {
        Todo::factory()->times(50)->create();
    }
}

```

--------------------------------

### Get Hash Field Expiration Time with Upstash Redis (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/hash/hexpiretime

This code snippet demonstrates how to use the Upstash Redis client in TypeScript to set a hash field, set its expiration time using HEXPIREAT, and then retrieve the expiration time using HEXPIRETIME. It handles cases where fields or keys might not exist or have no expiration.

```typescript
await redis.hset("my-key", "my-field", "my-value");
await redis.hexpireat("my-key", "my-field", Math.floor(Date.now() / 1000) + 10);
const expireTime = await redis.hexpiretime("my-key", "my-field");

console.log(expireTime); // e.g., [1697059200]
```

--------------------------------

### Set Hash Field Expiration Time with TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/hash/hexpireat

This example demonstrates how to use the HEXPIREAT command in TypeScript to set an expiration time for a specific field within a Redis hash. It first sets a field-value pair using HSET and then applies an expiration 10 seconds in the future using HEXPIREAT. The response indicates whether the expiration was successfully set.

```typescript
await redis.hset("my-key", "my-field", "my-value");
const expirationSet = await redis.hexpireat("my-key", "my-field", Math.floor(Date.now() / 1000) + 10);

console.log(expirationSet); // [1]
```

--------------------------------

### Deploy Supabase Function and Set Secrets

Source: https://upstash.com/docs/redis/quickstarts/supabase

This sequence of commands deploys the 'upstash-redis-counter' function to Supabase and sets its environment secrets. `supabase functions deploy` uploads the function, while `supabase secrets set` configures the necessary UPSTASH_REDIS_REST_URL and UPSTASH_REDIS_REST_TOKEN from the local .env file. These are essential for the function to connect to your Upstash Redis instance in production.

```bash
supabase functions deploy upstash-redis-counter --no-verify-jwt
supabase secrets set --env-file supabase/functions/upstash-redis-counter/.env
```

--------------------------------

### Build AWS SAM Application

Source: https://upstash.com/docs/redis/tutorials/using_aws_sam

This command builds the AWS SAM application, preparing it for deployment. It processes the template and code, creating artifacts needed for AWS Lambda.

```shell
sam build
```

--------------------------------

### Handle Incoming Weather Request (Elixir)

Source: https://upstash.com/docs/redis/quickstarts/elixir

This is the main controller function that receives user input (location text), fetches the weather information using the `fetch_weather` method, and renders the results. It handles both successful weather data retrieval and error cases.

```elixir
def home(conn, %{"text" => text}) do
    case fetch_weather(text) do
      {:ok, %{"location" => location, "temp" => temp_c, "condition" => condition_text}} ->
        render_home(conn, %Payload{weather: "#{condition_text}, #{temp_c}", location: location})
      {:error, reason} ->
        render_home(conn, %Payload{text: reason})
    end
  end
```

--------------------------------

### Serverless Framework Configuration for Upstash Redis

Source: https://upstash.com/docs/redis/tutorials/auto_complete_with_serverless_redis

This YAML configuration defines a serverless function using the Serverless Framework. It specifies the AWS provider, Node.js runtime, and environment variables, including the REDIS_URL. It also defines an HTTP API endpoint for the 'query' function.

```yaml
useDotenv: true
frameworkVersion: "2"

provider:
  name: aws
  runtime: nodejs14.x
  lambdaHashingVersion: 20201221
  environment:
    REDIS_URL: REPLACE_YOUR_REDIS_URL

functions:
  query:
    handler: handler.query
    events:
      - httpApi:
          path: /query
          method: get
          cors: true
```

--------------------------------

### Get Reverse Rank of Member in Sorted Set (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/zset/zrevrank

This code snippet demonstrates how to use the ZREVRANK command with Upstash Redis in TypeScript. It retrieves the rank of a specified member within a sorted set, ordered by score from highest to lowest. The function requires the key of the sorted set and the member whose rank is to be determined. The output is the integer rank of the member.

```typescript
const rank = await redis.rank("key", "member");
```

--------------------------------

### Scan Redis Database Keys (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/generic/scan

This snippet demonstrates how to use the SCAN command to retrieve keys from a Redis database. It initializes the scan with cursor '0' and an options object to match all keys. The response provides the next cursor and a list of matching keys, continuing until the cursor returns to '0'.

```typescript
const [cursor, keys] = await redis.scan(0, { match: "*" });
```

--------------------------------

### Remove Members from Sorted Set using Python Redis

Source: https://upstash.com/docs/redis/sdks/py/commands/zset/zrem

This Python code snippet demonstrates how to use the ZREM command with Upstash Redis to remove members from a sorted set. It first adds members using ZADD and then removes a specified member, returning the count of removed members. Ensure the 'redis' library is installed and configured to connect to your Upstash Redis instance.

```python
redis.zadd("myset", {"one": 1, "two": 2, "three": 3})

assert redis.zrem("myset", "one", "four") == 1
```

--------------------------------

### Enable Redis Keyspace Notifications (redis-cli)

Source: https://upstash.com/docs/redis/howto/keyspacenotifications

Enables keyspace notifications for hash commands using the redis-cli. This command connects to the Redis instance using TLS and the provided URL, then sets the `notify-keyspace-events` configuration to 'Kh'.

```bash
redis-cli --tls -u $UPSTASH_REDIS_CLI_URL config set notify-keyspace-events Kh
```

--------------------------------

### LRANGE Command Documentation

Source: https://upstash.com/docs/redis/sdks/ts/commands/list/lrange

This section details the LRANGE command, including its parameters, request structure, and response format.

```APIDOC
## LRANGE

### Description
Returns the specified elements of the list stored at key.

### Method
GET (or equivalent for Redis command execution)

### Endpoint
/websites/upstash-redis (Conceptual, actual execution via Redis client)

### Parameters
#### Path Parameters
None

#### Query Parameters
None

#### Request Body
- **key** (string) - Required - The key of the list.
- **start** (integer) - Required - The starting index of the range to return. Use negative numbers to specify offsets starting at the end of the list.
- **end** (integer) - Required - The ending index of the range to return. Use negative numbers to specify offsets starting at the end of the list.

### Request Example
```typescript
// Conceptual example using Upstash Redis client
await redis.lpush("key", "a", "b", "c");
const elements = await redis.lrange("key", 1, 2);
console.log(elements); // Expected output: ["b", "c"]
```

### Response
#### Success Response (200)
- **TValue[]** (array) - The list of elements in the specified range.

#### Response Example
```json
["b", "c"]
```
```

--------------------------------

### Configure Fixed Window Ratelimit with Upstash Redis

Source: https://upstash.com/docs/redis/sdks/ratelimit-py/algorithms

Sets up a Fixed Window ratelimiter using Upstash Redis. This algorithm divides time into fixed windows and counts requests within each window. It's computationally inexpensive but can allow bursts at window boundaries.

```python
from upstash_ratelimit import Ratelimit, FixedWindow
from upstash_redis import Redis

ratelimit = Ratelimit(
    redis=Redis.from_env(),
    limiter=FixedWindow(max_requests=10, window=10),
)
```

--------------------------------

### Configure Multiple Rate Limits in TypeScript

Source: https://upstash.com/docs/redis/sdks/ratelimit-ts/features

Demonstrates how to set up and use multiple rate limiters with different configurations (e.g., free and paid tiers) using the Upstash Redis SDK. This allows for granular control over request rates based on user type or identifier. It utilizes the sliding window limiter and enables analytics for dashboard monitoring.

```typescript
import { Redis } from "@upstash/redis";
import { Ratelimit } from "@upstash/ratelimit";

const redis = Redis.fromEnv();

const ratelimit = {
  free: new Ratelimit({
    redis,
    analytics: true,
    prefix: "ratelimit:free",
    limiter: Ratelimit.slidingWindow(10, "10s"),
  }),
  paid: new Ratelimit({
    redis,
    analytics: true,
    prefix: "ratelimit:paid",
    limiter: Ratelimit.slidingWindow(60, "10s"),
  }),
};

await ratelimit.free.limit(ip);
// or for a paid user you might have an email or userId available:
await ratelimit.paid.limit(userId);
```

--------------------------------

### Node.js Script to Initialize Redis Sorted Set with Prefixes

Source: https://upstash.com/docs/redis/tutorials/auto_complete_with_serverless_redis

This Node.js script initializes a Redis Sorted Set named 'terms' with country names and their prefixes. It reads country data, generates all possible prefixes for each country name, and adds them to the sorted set with a score of 0. Prefixes are marked with an asterisk to distinguish them from full country names during retrieval.

```javascript
require('dotenv').config()
var Redis = require("ioredis");

var countries = [
    {"name": "Afghanistan", "code": "AF"},
    {"name": "Åland Islands", "code": "AX"},
    {"name": "Albania", "code": "AL"},
    {"name": "Algeria", "code": "DZ"},
    ...
]
var client = new Redis(process.env.REDIS_URL);

for (const country of countries) {
    let term = country.name.toUpperCase();
    let terms = [];

    for (let i = 1; i < term.length; i++) {
        terms.push(0);
        terms.push(term.substring(0, i));
    }
    terms.push(0);
    terms.push(term + "*");
    (async () => {
        await client.zadd("terms", ...terms)
    })();
}
```

--------------------------------

### Configure Upstash Redis Stdio MCP Server (JSON)

Source: https://upstash.com/docs/redis/integrations/mcp

This configuration sets up a direct Stdio MCP server for Upstash Redis. It specifies the command to run the Upstash MCP server with provided email and API key. This is suitable for direct server-to-server communication.

```json
{
  "mcpServers": {
    "upstash": {
      "command": "npx",
      "args": [
        "-y",
        "@upstash/mcp-server",
        "run",
        "<UPSTASH_EMAIL>",
        "<UPSTASH_API_KEY>"
      ]
    }
  }
}
```

```json
{
  "servers": {
    "upstash": {
      "type": "stdio",
      "command": "npx",
      "args": [
        "-y",
        "@upstash/mcp-server",
        "run",
        "<UPSTASH_EMAIL>",
        "<UPSTASH_API_KEY>"
      ]
    }
  }
}
```

--------------------------------

### Upstash Redis with TypeScript SDK in Cloudflare Workers

Source: https://context7.com/context7/upstash-redis/llms.txt

This TypeScript code demonstrates how to use the Upstash Redis SDK within a Cloudflare Worker. It shows how to initialize the client using environment variables for credentials and implements rate limiting and caching logic using Redis commands.

```typescript
// worker.ts - Cloudflare Worker example
import { Redis } from "@upstash/redis/cloudflare";

export default {
  async fetch(request: Request, env: Env): Promise<Response> {
    const redis = new Redis({
      url: env.UPSTASH_REDIS_REST_URL,
      token: env.UPSTASH_REDIS_REST_TOKEN,
    });

    // Rate limiting check
    const ip = request.headers.get("CF-Connecting-IP") || "unknown";
    const count = await redis.incr(`rate:${ip}`);

    if (count === 1) {
      await redis.expire(`rate:${ip}`, 60); // 60 second window
    }

    if (count > 10) {
      return new Response("Rate limit exceeded", { status: 429 });
    }

    // Cache response
    const cacheKey = `cache:${new URL(request.url).pathname}`;
    let cached = await redis.get(cacheKey);

    if (!cached) {
      cached = { data: "expensive computation result", timestamp: Date.now() };
      await redis.set(cacheKey, JSON.stringify(cached), { ex: 300 });
    }

    return new Response(JSON.stringify(cached), {
      headers: { "Content-Type": "application/json" },
    });
  },
};
```

--------------------------------

### Implementing Multiple Rate Limits with Upstash Redis

Source: https://upstash.com/docs/redis/sdks/ratelimit-py/features

Shows how to manage different rate limiting policies for distinct user groups (e.g., free vs. paid) using separate `Ratelimit` instances with custom prefixes. This allows for granular control over API access based on subscription tiers or other criteria. It utilizes the `upstash_ratelimit` and `upstash_redis` libraries.

```python
from upstash_ratelimit import Ratelimit, SlidingWindow
from upstash_redis import Redis

class MultiRL:
    def __init__(self) -> None:
        redis = Redis.from_env()
        self.free = Ratelimit(
            redis=redis,
            limiter=SlidingWindow(max_requests=10, window=10),
            prefix="ratelimit:free",
        )

        self.paid = Ratelimit(
            redis=redis,
            limiter=SlidingWindow(max_requests=60, window=10),
            prefix="ratelimit:paid",
        )

# Create a new ratelimiter, that allows 10 requests per 10 seconds
ratelimit = MultiRL()

ratelimit.free.limit("userIP")
ratelimit.paid.limit("userIP")
```

--------------------------------

### Run Container Locally with Docker

Source: https://upstash.com/docs/redis/tutorials/cloud_run_sessions

This command configures Docker to authenticate with Google Container Registry and then runs the previously built container image locally. It maps port 8080 on your host machine to port 8080 within the container, allowing you to access the web service.

```bash
gcloud auth configure-docker

docker run -d -p 8080:8080 gcr.io/cloud-run-sessions/main:v0.1
```

--------------------------------

### Configure Upstash Redis Credentials

Source: https://upstash.com/docs/redis/tutorials/python_multithreading

Set your Upstash Redis URL and token in a .env file for authentication. This file is essential for the application to connect to your Redis instance.

```bash
UPSTASH_REDIS_REST_URL=your_upstash_redis_url
UPSTASH_REDIS_REST_TOKEN=your_upstash_redis_token
```

--------------------------------

### Deploy AWS CDK Application

Source: https://upstash.com/docs/redis/quickstarts/aws-lambda

Deploys the AWS CDK application to your AWS account. This sequence of commands synthesizes the CloudFormation template, bootstraps the CDK environment if necessary, and then deploys the stack, making the Lambda function and its URL available.

```shell
cdk synth
cdk bootstrap
cdk deploy
```

--------------------------------

### Publish JSON to QStash using Client (TypeScript)

Source: https://upstash.com/docs/redis/howto/vercelintegration

Publish a JSON message to a specified URL using the Upstash QStash client. Requires QSTASH_TOKEN environment variable for authentication. The response is captured but not explicitly handled in this snippet.

```typescript
import { Client } from "@upstash/qstash";

const client = new Client({
  token: process.env.QSTASH_TOKEN,
});

const res = await client.publishJSON({
  url: "https://my-api...",
  body: {
    hello: "world",
  },
});
```

--------------------------------

### Create New Supabase Function

Source: https://upstash.com/docs/redis/quickstarts/supabase

This command creates a new Supabase function named 'upstash-redis-counter' in your project. It utilizes the Supabase CLI to scaffold a new function, which will serve as the entry point for your serverless logic. This is a foundational step before adding custom code.

```shell
supabase functions new upstash-redis-counter
```

--------------------------------

### Node.js Server with Redis Counter

Source: https://upstash.com/docs/redis/tutorials/aws_app_runner_with_redis

A Node.js script that initializes a Redis client using an environment variable, increments a counter in Redis for each incoming request, and returns the current count as the response. It requires the 'ioredis' package and a REDIS_URL environment variable.

```javascript
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

--------------------------------

### Listen for All Keyspace Events (redis-cli)

Source: https://upstash.com/docs/redis/howto/keyspacenotifications

Subscribes to all keyspace and keyevent notification channels using redis-cli. This command is useful for testing and observing the events triggered by the configuration. It uses the `--csv` option for comma-separated output.

```bash
redis-cli --tls -u $UPSTASH_REDIS_CLI_URL --csv psubscribe '__key*__:*'
```

--------------------------------

### Configure Upstash Redis Environment Variables

Source: https://upstash.com/docs/redis/quickstarts/ion

Sets the Upstash Redis connection URL and token in the .env file. These environment variables are crucial for the application to connect to the Redis instance.

```env
UPSTASH_REDIS_REST_URL=<YOUR_URL>
UPSTASH_REDIS_REST_TOKEN=<YOUR_TOKEN>
```

--------------------------------

### Next.js Frontend for Roadmap Voting App

Source: https://upstash.com/docs/redis/tutorials/roadmapvotingapp

This JavaScript code defines the main `Home` component for the roadmap voting application. It handles user interactions such as refreshing data, voting for features, adding new features, and subscribing for release notifications via email. It utilizes `react-toastify` for user feedback and `fetch` to communicate with backend APIs.

```javascript
import Head from 'next/head'
import { ToastContainer, toast } from 'react-toastify';
import * as React from "react";

class Home extends React.Component {
    // ... placeholder for component logic ...
    refreshData() {
        fetch("api/list")
            .then(res => res.json())
            .then(
                (result) => {
                    this.setState({
                        isLoaded: true,
                        items: result.body
                    });
                    this.inputNewFeature.current.value = "";
                },
                (error) => {
                    this.setState({
                        isLoaded: true,
                        error
                    });
                }
            )
    }

    vote(event, title) {
        const requestOptions = {
            method: 'POST',
            headers: {'Content-Type': 'application/json'},
            body: JSON.stringify({"title": title})
        };
        console.log(requestOptions);
        fetch('api/vote', requestOptions) 
            .then(response => response.json()).then(data => {
                console.log(data)
                if(data.error) {
                    toast.error(data.error, {hideProgressBar: true, autoClose: 3000});
                } else {
                    this.refreshData()
                }
        })
    }

    handleNewFeature(event) {
        const requestOptions = {
            method: 'POST',
            headers: {'Content-Type': 'application/json'},
            body: JSON.stringify({"title": this.inputNewFeature.current.value})
        };
        fetch('api/create', requestOptions) 
            .then(response => response.json()).then(data => {
            if(data.error) {
                toast.error(data.error, {hideProgressBar: true, autoClose: 5000});
            } else {
                toast.info("Your feature has been added to the list.", {hideProgressBar: true, autoClose: 3000});
                this.refreshData()
            }
        });
        event.preventDefault();
    }

    handleNewEmail(event) {
        const requestOptions = {
            method: 'POST',
            headers: {'Content-Type': 'application/json'},
            body: JSON.stringify({"email": this.inputEmail.current.value})
        };
        console.log(requestOptions);
        fetch('api/addemail', requestOptions) 
            .then(response => response.json()).then(data => {
            if(data.error) {
                toast.error(data.error, {hideProgressBar: true, autoClose: 3000});
            } else {
                toast.info("Your email has been added to the list.", {hideProgressBar: true, autoClose: 3000});
                this.refreshData()
            }
        });
        event.preventDefault();
    }
}
export default Home;

```

--------------------------------

### Package.json for Google Cloud Function Dependencies

Source: https://upstash.com/docs/redis/quickstarts/google-cloud-functions

This package.json file specifies the necessary dependencies for a Google Cloud Function interacting with Upstash Redis. It includes '@google-cloud/functions-framework' for the function runtime and '@upstash/redis' for Redis client functionality.

```json
{
  "dependencies": {
    "@google-cloud/functions-framework": "^3.0.0",
    "@upstash/redis": "^1.31.6"
  }
}
```

--------------------------------

### Execute KEYS Command with Pattern (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/generic/keys

This snippet demonstrates how to use the redis.keys() method in TypeScript to fetch keys matching a specific pattern (e.g., 'prefix*'). It's important to note the warning against using this in production.

```typescript
const keys = await redis.keys("prefix*");
```

--------------------------------

### Deploy to Production Stage

Source: https://upstash.com/docs/redis/quickstarts/sst-v2

Before deploying to production, set the Upstash Redis secrets for the `prod` stage using `npx sst secrets set`. Once the secrets are configured, deploy your SST application to the production environment with `npx sst deploy --stage prod`. After deployment, you can access your application's API endpoint at the `SiteUrl` outputted by SST.

```shell
npx sst secrets set --stage prod UPSTASH_REDIS_REST_URL <YOUR_URL>
npx sst secrets set --stage prod UPSTASH_REDIS_REST_TOKEN <YOUR_TOKEN>
npx sst deploy --stage prod
```

--------------------------------

### Python Redis ZINTER Simple Intersection

Source: https://upstash.com/docs/redis/sdks/py/commands/zset/zinter

Demonstrates a basic intersection of two sorted sets using the ZINTER command in Python. It adds elements to two keys and then finds their common elements.

```python
redis.zadd("key1", {"a": 1, "b": 2, "c": 3})

redis.zadd("key2", {"c": 3, "d": 4, "e": 5})

result = redis.zinter(["key1", "key2"])

assert result == ["c"]
```

--------------------------------

### Calculate Sliding Window Ratelimit Approximation

Source: https://upstash.com/docs/redis/sdks/ratelimit-py/algorithms

Demonstrates the calculation for a Sliding Window ratelimit approximation. This method uses a rolling window and weights requests from previous windows, offering better boundary handling than Fixed Window but with higher computational cost.

```python
limit = 10

# 4 request from the old window, weighted + requests in current window
rate = 4 * ((60 - 15) / 60) + 5 = 8

return rate < limit # True means we should allow the request
```

--------------------------------

### LPUSH Command in Python

Source: https://upstash.com/docs/redis/sdks/py/commands/list/lpush

Demonstrates how to use the LPUSH command to add multiple elements to the head of a list in Upstash Redis using Python. It includes assertions to verify the operation's success and the final state of the list. Requires the 'redis' library.

```python
assert redis.lpush("mylist", "one", "two", "three") == 3

assert lrange("mylist", 0, -1) == ["three", "two", "one"]
```

--------------------------------

### Run Test Script

Source: https://upstash.com/docs/redis/tutorials/python_session

Executes a Python script designed to test the functionality of the FastAPI application, including login, profile access, and logout endpoints. This helps verify the session management system.

```python
python test_script.py
```

--------------------------------

### Add Redisson Dependency to Maven Project

Source: https://upstash.com/docs/redis/tutorials/redisson

This snippet shows the Maven dependency required to include the Redisson client library in your project. Ensure you have a Maven project set up.

```xml
<dependency>
    <groupId>org.redisson</groupId>
    <artifactId>redisson</artifactId>
    <version>3.15.4</version>
</dependency>
```

--------------------------------

### Pub/Sub and Monitoring via REST

Source: https://context7.com/context7/upstash-redis/llms.txt

Interact with Redis Pub/Sub capabilities and monitor database activity using Server-Sent Events (SSE) through the REST API.

```APIDOC
## POST /pub/<channel>

### Description
Publishes a message to a specified channel.

### Method
POST

### Endpoint
`https://<your-domain>.upstash.io/pub/<channel>`

### Parameters
#### Path Parameters
- **channel** (string) - Required - The channel to publish the message to.

#### Query Parameters
None

#### Request Body
- **message** (string) - Required - The message content to publish.

### Request Example
```bash
curl -X POST -d 'message=Hello, subscribers!' \
  https://us1-merry-cat-32748.upstash.io/pub/news \
  -H "Authorization: Bearer <YOUR_TOKEN>"
```

### Response
#### Success Response (200)
- **result** (integer) - The number of clients that received the message.

#### Response Example
```json
{
  "result": 5
}
```

---

## GET /sub/<channel>

### Description
Subscribes to a channel to receive messages via Server-Sent Events (SSE).

### Method
GET

### Endpoint
`https://<your-domain>.upstash.io/sub/<channel>`

### Parameters
#### Path Parameters
- **channel** (string) - Required - The channel to subscribe to.

#### Query Parameters
None

#### Request Body
None

### Request Example
```bash
# This command would typically be used in a client that can handle SSE streams.
# Example using curl (will stream data):
curl https://us1-merry-cat-32748.upstash.io/sub/news \
  -H "Authorization: Bearer <YOUR_TOKEN>"
```

### Response
#### Success Response (200)
- **Data Stream** - The response is a stream of Server-Sent Events, where each event contains a message published to the subscribed channel.

#### Response Example (SSE format)
```
data: {"message": "Hello, subscribers!"}

```
```

--------------------------------

### Execute Custom Redis Commands

Source: https://upstash.com/docs/redis/sdks/py/features

Shows how to execute Redis commands that are not explicitly implemented in the client library. The `execute` function can take a list representing the command and its arguments.

```python
redis.execute(["XLEN", "test_stream"])
```

--------------------------------

### Execute Redis Command with Token as Query Parameter (cURL)

Source: https://upstash.com/docs/redis/features/restapi

Shows an alternative way to execute a Redis SET command using cURL by passing the authorization token as a query parameter (`_token`).

```shell
curl https://us1-merry-cat-32748.upstash.io/set/foo/bar?_token=2553feg6a2d9842h2a0gcdb5f8efe9934
```

--------------------------------

### Fastly Compute@Edge JavaScript with Upstash Redis

Source: https://upstash.com/docs/redis/quickstarts/fastlycompute

This JavaScript code snippet defines a Fetch API handler for Fastly Compute@Edge. It initializes a Redis client using environment variables for the URL and token, and specifies the 'upstash' backend. It then increments a Redis counter and returns the updated count in the response.

```javascript
import { Redis } from "@upstash/redis/fastly";

addEventListener("fetch", (event) => event.respondWith(handleRequest(event)));

async function handleRequest(event) {
  const redis = new Redis({
    url: "UPSTASH_REDIS_REST_URL",
    token: "UPSTASH_REDIS_REST_TOKEN",
    backend: "upstash",
  });
  const data = await redis.incr("count");
  return new Response("View Count:" + data, { status: 200 });
}
```

--------------------------------

### Basic Command Execution (GET/POST)

Source: https://upstash.com/docs/redis/features/restapi

Execute Redis commands by appending them to the REST URL. For commands involving values, POST can be used with the value in the request body.

```APIDOC
## GET/POST /COMMAND/arg1/arg2/...

### Description
Execute a Redis command by specifying the command and its arguments as path parameters.
For commands where the value is complex (like JSON or binary), use an HTTP POST request with the value as the request body.

### Method
GET or POST (depending on the command and value encoding)

### Endpoint
`REST_URL/COMMAND/arg1/arg2/...`

### Parameters
#### Path Parameters
- **COMMAND** (string) - Required - The name of the Redis command (e.g., `GET`, `SET`, `MGET`).
- **arg1, arg2, ...** (string) - Optional - Arguments for the Redis command, separated by `/`.

#### Query Parameters
- **_token** (string) - Optional - The authorization token can be provided as a query parameter.
- **EX** (integer) - Optional - Example query parameter for setting expiration.

#### Request Body
- **$VALUE** (any) - Required for POST requests when the value is complex and cannot be part of the URL. This value is appended as the last parameter of the command.

### Request Example (GET)
```shell
curl https://YOUR_UPSTASH_URL/get/foo \
 -H "Authorization: Bearer YOUR_TOKEN"
```

### Request Example (POST with value in body)
```shell
curl -X POST -d 'some_value' https://YOUR_UPSTASH_URL/set/foo \
 -H "Authorization: Bearer YOUR_TOKEN"
```

### Request Example (POST with value and EX)
```shell
curl -X POST -d '$VALUE' https://YOUR_UPSTASH_URL/set/foo?EX=100 \
 -H "Authorization: Bearer YOUR_TOKEN"
```

### Response
#### Success Response (200)
- **result** (any) - The result of the Redis command execution. Can be null, integer, string, or array.

#### Response Example
```json
{
  "result": "OK"
}
```

#### Error Response (400, 401)
- **error** (string) - A message describing the error.
```

--------------------------------

### Configure Redix Connection from Environment Variable (Elixir)

Source: https://upstash.com/docs/redis/quickstarts/elixir

Parses the 'REDIS_URL' environment variable using a regular expression to extract connection details such as password, host, and port. This method is used within the 'application.ex' file to dynamically configure the Redix client for Upstash Redis.

```elixir
def start(_type, _args) do
  [_, password, host, port] = Regex.run(
    ~r{(.+):(.+)@(.+):(\d+)},
    System.get_env("REDIS_URL"),
    capture: :all_but_first
  )
  port = elem(Integer.parse(port), 0)
  # ...
end
```

--------------------------------

### Set Upstash Redis Secrets

Source: https://upstash.com/docs/redis/quickstarts/sst-v2

These commands are used to store your Upstash Redis connection URL and token as secrets within the SST environment. Replace `<YOUR_URL>` and `<YOUR_TOKEN>` with your actual Upstash Redis credentials. These secrets will be accessible by your application.

```shell
npx sst secrets set UPSTASH_REDIS_REST_URL <YOUR_URL>
npx sst secrets set UPSTASH_REDIS_REST_TOKEN <YOUR_TOKEN>
```

--------------------------------

### Basic Todo Controller Index Method

Source: https://upstash.com/docs/redis/tutorials/laravel_caching

Implements the `index` method in the `TodoController` to retrieve and return all records from the 'todos' table. This is a fundamental part of the API for listing resources.

```php
<?php

namespace App\Http\Controllers;

use App\Models\Todo;
use Illuminate\Http\Request;

class TodoController extends Controller
{
    /**
     * Display a listing of the resource.
     */
    public function index()
    {
        return Todo::all();
    }
    ...
}

```

--------------------------------

### Fetch Weather Data from Cache (Elixir)

Source: https://upstash.com/docs/redis/quickstarts/elixir

This method queries Upstash Redis for cached weather data using a specific key format ('weather:#{location}'). It returns the cached data if found and decoded, or an error if not found or if the Redis command fails.

```elixir
defp fetch_weather_from_cache(location) do
    case Redix.command(:redix, ["GET", "weather:#{location}"]) do
      {:ok, nil} ->
        {:error, :not_found}
      {:ok, cached_weather_json} ->
        {:ok, Jason.decode!(cached_weather_json)}
      {:error, _reason} ->
        {:error, "Failed to fetch weather data from cache."}
    end
  end
```

--------------------------------

### Configure Fly.io Application Environment Variable

Source: https://upstash.com/docs/redis/quickstarts/fly

This TOML snippet shows how to configure environment variables for a Fly.io application. Specifically, it adds the `REDIS_URL` environment variable within the `[env]` section of the `fly.toml` file, which is crucial for the application to connect to the Upstash Redis instance.

```toml
[env]
  REDIS_URL = "<your-upstash-redis-url>"
```

--------------------------------

### Enable Auto IP Deny List Protection in TypeScript

Source: https://upstash.com/docs/redis/sdks/ratelimit-ts/traffic-protection

This snippet demonstrates how to initialize the Ratelimit with the Auto IP Deny List feature enabled. It requires the `redis` client and a `limiter` configuration. Setting `enableProtection` to `true` activates the feature.

```typescript
const ratelimit = new Ratelimit({
  redis: Redis.fromEnv(),
  limiter: Ratelimit.slidingWindow(10, "10 s"),
  enableProtection: true,
});
```

--------------------------------

### Redis SET with NX and XX in Python

Source: https://upstash.com/docs/redis/sdks/py/commands/string/set

Demonstrates conditional setting of a key using the NX (set only if not exists) and XX (set only if exists) options. These options control whether the key is set based on its current existence.

```python
# Only set the key if it does not already exist.
assert redis.set("key", "value", nx=True) == False

# Only set the key if it already exists.
assert redis.set("key", "value", xx=True) == True
```

--------------------------------

### Redis ZUNIONSTORE Basic Union - Python

Source: https://upstash.com/docs/redis/sdks/py/commands/zset/zunionstore

Demonstrates the basic usage of the ZUNIONSTORE command to find the union of two sets and store the result in a new key. It adds elements to 'key1' and 'key2', performs the union, and asserts the size of the resulting set.

```python
redis.zadd("key1", {"a": 1, "b": 2, "c": 3})

redis.zadd("key2", {"c": 3, "d": 4, "e": 5})

result = redis.zunionstore(["key1", "key2"])

assert result == 5
```

--------------------------------

### Node.js Consumer with Bull and Upstash Redis

Source: https://upstash.com/docs/redis/tutorials/job_processing

This Node.js code sets up a consumer using the Bull library to process jobs from an 'employee registration' queue stored in Upstash Redis. It configures connection details and processing logic, including optional settings to manage Upstash quotas. Remember to replace Redis credentials and adjust TLS settings as needed.

```javascript
var Queue = require("bull");

var settings = {
  stalledInterval: 300000, // How often check for stalled jobs (use 0 for never checking).
  guardInterval: 5000, // Poll interval for delayed jobs and added jobs.
  drainDelay: 300, // A timeout for when the queue is in drained state (empty waiting for jobs).
};

var taskQueue = new Queue(
  "employee registration",
  {
    redis: {
      port: 32016,
      host: "us1-upward-ant-32016.upstash.io",
      password: "ake4ff120d6b4216df220736be7eab087",
      tls: {},
    },
  },
  settings
);

taskQueue
  .process(function (job, done) {
    console.log(job.data);
    // TODO process the new employee event
    done();
  })
  .catch((err) => {
    console.log(err);
  });

```

--------------------------------

### Configure Sliding Window Ratelimit with Upstash Redis

Source: https://upstash.com/docs/redis/sdks/ratelimit-py/algorithms

Initializes a Sliding Window ratelimiter with Upstash Redis. This algorithm uses a rolling window for more accurate rate limiting across window boundaries, though it is more computationally intensive.

```python
from upstash_ratelimit import Ratelimit, SlidingWindow
from upstash_redis import Redis

ratelimit = Ratelimit(
    redis=Redis.from_env(),
    limiter=SlidingWindow(max_requests=10, window=10),
)
```

--------------------------------

### ZINTERSTORE with Weights (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/zset/zinterstore

Shows how to use the ZINTERSTORE command with weights applied to the intersecting sets. This allows for custom weighting during the intersection calculation. The `weights` option takes an array of numbers corresponding to the keys provided.

```typescript
await redis.zadd(
    "key1", 
    { score: 1, member: "member1" },
)
await redis.zadd(
    "key2",
    { score: 1, member: "member1" },
    { score: 2, member: "member2" },
)
const res = await redis.zinterstore(
    "destination",
    2,
    ["key1", "key2"],
    { weights: [2, 3] },
);
console.log(res) // 1
```

--------------------------------

### ZDIFFSTORE

Source: https://upstash.com/docs/redis/sdks/ts/commands/zset/zdiffstore

Writes the difference between sets to a new key. The command takes a destination key, the number of keys to compare, and the keys themselves as arguments. It returns the number of elements in the resulting set.

```APIDOC
## ZDIFFSTORE

### Description
Writes the difference between sets to a new key.

### Method
ZDIFFSTORE

### Endpoint
/websites/upstash-redis

### Parameters
#### Path Parameters
None

#### Query Parameters
None

#### Request Body
- **destination** (string) - Required - The key to write the difference to.
- **keys** (integer) - Required - How many keys to compare.
- **keys** (...string[]) - Required - The keys to compare.

### Request Example
```ts
const values = await redis.zdiffstore("destination", 2, "key1", "key2");
```

### Response
#### Success Response (200)
- The number of elements in the resulting set. (integer) - Required

#### Response Example
```json
{
  "example": "10"
}
```
```

--------------------------------

### Set up SRH via Docker Compose

Source: https://upstash.com/docs/redis/sdks/ts/developing

This Docker Compose configuration sets up a Redis service and a Serverless Redis HTTP (SRH) service. SRH will proxy connections to the local Redis instance within the Docker network. This configuration is suitable for environments like Kubernetes or local development with Docker Compose.

```yaml
version: "3" 
services:
  redis:
    image: redis
    ports:
      - "6379:6379"
  serverless-redis-http:
    ports:
      - "8079:80"
    image: hiett/serverless-redis-http:latest
    environment:
      SRH_MODE: env
      SRH_TOKEN: example_token
      SRH_CONNECTION_STRING: "redis://redis:6379" # Using `redis` hostname since they're in the same Docker network.
```

--------------------------------

### Upstash Redis LPOS Command - Basic Usage (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/list/lpos

Demonstrates the basic usage of the LPOS command in TypeScript to find the index of an element within a Redis list. It first pushes elements into a list and then uses LPOS to retrieve the index of a specific element.

```typescript
await redis.rpush("key", "a", "b", "c"); 
const index = await redis.lpos("key", "b");
console.log(index); // 1
```

--------------------------------

### Execute KEYS Command to Match All Keys (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/generic/keys

This snippet shows how to retrieve all keys in the database using redis.keys('*') in TypeScript. This operation can be very time-consuming and is not recommended for production environments.

```typescript
const keys = await redis.keys("*");
```

--------------------------------

### Access Koyeb Runtime Logs

Source: https://upstash.com/docs/redis/quickstarts/koyeb

Streams the runtime logs of a running Koyeb service. This is essential for debugging application behavior after deployment.

```bash
koyeb service logs example-koyeb-upstash/example-koyeb-upstash -t runtime
```

--------------------------------

### Redis Command Compatibility

Source: https://upstash.com/docs/redis/overall/rediscompatibility

This section details the Redis commands supported by Upstash, categorized by data structure. It includes support for versions up to 6.2 and progressive adoption of features from 7.0 and 7.2.

```APIDOC
## Redis Command Compatibility

### Description
Upstash supports the Redis client protocol up to version `6.2`. We are also gradually adding changes introduced in versions `7.0` and `7.2`, such as `EXPIRETIME`, `LMPOP`, `ZINTERCARD` and `EVAL_RO`.

The following table shows the most recent list of the supported Redis commands:

| Feature | Supported? | Supported Commands |
|---|---|---|
| [String](https://redis.io/commands/?group=string) | ✅ | APPEND - DECR - DECRBY - GET - GETDEL - GETEX - GETRANGE - GETSET - INCR - INCRBY - INCRBYFLOAT - MGET - MSET - MSETNX - PSETEX - SET - SETEX - SETNX - SETRANGE - STRLEN |
| [Bitmap](https://redis.io/commands/?group=bitmap) | ✅ | BITCOUNT - BITFIELD - BITFIELD_RO - BITOP - BITPOS - GETBIT - SETBIT |
| [Hash](https://redis.io/commands/?group=hash) | ✅ | HDEL - HEXISTS - HGET - HGETALL - HINCRBY - HINCRBYFLOAT - HKEYS - HLEN - HMGET - HMSET - HSCAN - HSET - HSETNX - HSTRLEN - HRANDFIELD - HVALS |
| [List](https://redis.io/commands/?group=list) | ✅ | BLMOVE - BLMPOP - BLPOP - BRPOP - BRPOPLPUSH - LINDEX - LINSERT - LLEN - LMOVE - LMPOP - LPOP - LPOS - LPUSH - LPUSHX - LRANGE - LREM - LSET - LTRIM - RPOP - RPOPLPUSH - RPUSH - RPUSHX |
| [Set](https://redis.io/commands/?group=set) | ✅ | SADD - SCARD - SDIFF - SDIFFSTORE - SINTER - SINTERCARD - SINTERSTORE - SISMEMBER - SMEMBERS - SMISMEMBER - SMOVE - SPOP - SRANDMEMBER - SREM - SSCAN - SUNION - SUNIONSTORE |
| [SortedSet](https://redis.io/commands/?group=sorted_set) | ✅ | BZMPOP - BZPOPMAX - BZPOPMIN - ZADD - ZCARD - ZCOUNT - ZDIFF - ZDIFFSTORE - ZINCRBY - ZINTER - ZINTERCARD - ZINTERSTORE - ZLEXCOUNT - ZMPOP - ZMSCORE - ZPOPMAX - ZPOPMIN - ZRANDMEMBER - ZRANGE - ZRANGESTORE - ZRANGEBYLEX - ZRANGEBYSCORE - ZRANK - ZREM - ZREMRANGEBYLEX - ZREMRANGEBYRANK - ZREMRANGEBYSCORE - ZREVRANGE - ZREVRANGEBYLEX - ZREVRANGEBYSCORE - ZREVRANK - ZSCAN - ZSCORE - ZUNION - ZUNIONSTORE |
| [Geo](https://redis.io/commands/?group=geo) | ✅ | GEOADD - GEODIST - GEOHASH - GEOPOS - GEORADIUS - GEORADIUS_RO - GEORADIUSBYMEMBER - GEORADIUSBYMEMBER_RO - GEOSEARCH - GEOSEARCHSTORE |
```

--------------------------------

### Add Jedis Dependency to Maven POM

Source: https://upstash.com/docs/redis/tutorials/serverless_java_redis

Adds the Jedis client library as a dependency to the Maven project's pom.xml file. Jedis is used for interacting with Redis.

```xml
    <dependency>
        <groupId>redis.clients</groupId>
        <artifactId>jedis</artifactId>
        <version>3.6.0</version>
    </dependency>
```

--------------------------------

### SDIFFSTORE

Source: https://upstash.com/docs/redis/sdks/py/commands/set/sdiffstore

Computes the difference between sets and stores the result in a new set. It takes a destination key and one or more source set keys as arguments.

```APIDOC
## SDIFFSTORE

### Description
Writes the difference between sets to a new set.

### Method
POST

### Endpoint
/websites/upstash-redis

### Parameters
#### Query Parameters
- **destination** (str) - Required - The key of the set to store the resulting set in.
- **keys** (*List[str]) - Required - The keys of the sets to perform the difference operation on.

### Request Example
```json
{
  "command": "SDIFFSTORE",
  "args": ["destination_key", "key1", "key2"]
}
```

### Response
#### Success Response (200)
- **result** (int) - The number of elements in the resulting set.

#### Response Example
```json
{
  "result": 2
}
```
```

--------------------------------

### Configure Token Bucket Ratelimit with Upstash Redis

Source: https://upstash.com/docs/redis/sdks/ratelimit-py/algorithms

Sets up a Token Bucket ratelimiter using Upstash Redis. This algorithm smooths request bursts by consuming tokens from a bucket that refills at a constant rate, allowing for controlled processing and higher initial bursts.

```python
from upstash_ratelimit import Ratelimit, TokenBucket
from upstash_redis import Redis

ratelimit = Ratelimit(
    redis=Redis.from_env(),
    limiter=TokenBucket(max_tokens=10, refill_rate=5, interval=10),
)
```

--------------------------------

### Execute BITFIELD and BITFIELD_RO Commands

Source: https://upstash.com/docs/redis/sdks/py/features

Demonstrates how to use the BITFIELD and BITFIELD_RO commands via Python. These commands allow for efficient manipulation of Redis bitmaps. The `execute` function is used to run the chained commands.

```python
redis.bitfield("test_key") \
  .incrby(encoding="i8", offset=100, increment=100) \
  .overflow("SAT") \
  .incrby(encoding="i8", offset=100, increment=100) \
  .execute()

redis.bitfield_ro("test_key_2") \
  .get(encoding="u8", offset=0) \
  .get(encoding="u8", offset="#1") \
  .execute()
```

--------------------------------

### Retrieve All Hash Values in Python

Source: https://upstash.com/docs/redis/sdks/py/commands/hash/hvals

This Python code snippet demonstrates how to set a hash with multiple fields and then retrieve all its values using the `hvals` command. It assumes a Redis client instance is available and configured.

```python
redis.hset("myhash", values={
    "field1": "Hello",
    "field2": "World"
  })

assert redis.hvals("myhash") == ["Hello", "World"]
```

--------------------------------

### Integrate SRH in GitHub Actions

Source: https://upstash.com/docs/redis/sdks/ts/developing

This GitHub Actions workflow demonstrates how to use Serverless Redis HTTP (SRH) within a CI pipeline. It sets up Redis and SRH as services within a job, allowing tests (in this case, the @upstash/redis test suite) to run against SRH, which then connects to the Redis service.

```yaml
name: Test @upstash/redis compatibility
on:
  push:
  workflow_dispatch:

env:
  SRH_TOKEN: example_token

jobs:
  container-job:
    runs-on: ubuntu-latest
    container: denoland/deno
    services:
      redis:
        image: redis/redis-stack-server:6.2.6-v6 # 6.2 is the Upstash compatible Redis version
      srh:
        image: hiett/serverless-redis-http:latest
        env:
          SRH_MODE: env # We are using env mode because we are only connecting to one server.
          SRH_TOKEN: ${{ env.SRH_TOKEN }}
          SRH_CONNECTION_STRING: redis://redis:6379

    steps:
      # You can place your normal testing steps here. In this example, we are running SRH against the upstash/upstash-redis test suite.
      - name: Checkout code
        uses: actions/checkout@v3
        with:
          repository: upstash/upstash-redis

      - name: Run @upstash/redis Test Suite
        run: deno test -A ./pkg
        env:
          UPSTASH_REDIS_REST_URL: http://srh:80
          UPSTASH_REDIS_REST_TOKEN: ${{ env.SRH_TOKEN }}
```

--------------------------------

### TypeScript: Basic Write and Read Operations

Source: https://upstash.com/docs/redis/howto/readyourwrites

Demonstrates basic write and read operations using the Upstash Redis TypeScript SDK. This snippet shows how to set a key-value pair and then retrieve its value. It's important to note that without explicit sync token management, there's a small chance of reading stale data if the read request is served by a replica that hasn't yet received the write.

```typescript
import { Redis } from "@upstash/redis";
import { nanoid } from "nanoid";

export const writeRequest = async () => {
  const redis = Redis.fromEnv();
  const randomKey = nanoid();
  await redis.set(randomKey, "value");
  return randomKey;
};

export const readRequest = async (randomKey: string) => {
  const redis = Redis.fromEnv();
  const value = await redis.get(randomKey);
  return value;
};

// Example of calling these functions in sequence:
// const randomKey = await writeRequest();
// await readRequest(randomKey);
```

--------------------------------

### Enable Deny List Protection in Ratelimit Client

Source: https://upstash.com/docs/redis/sdks/ratelimit-ts/traffic-protection

This code snippet demonstrates how to initialize the Ratelimit client with the `enableProtection` option set to `true`. This enables the deny list functionality, allowing the client to check against blocked IPs, user agents, and countries before processing requests. It assumes you have already configured the Redis client.

```tsx
const ratelimit = new Ratelimit({
  redis: Redis.fromEnv(),
  limiter: Ratelimit.slidingWindow(10, "10 s"),
  enableProtection: true,
  analytics: true
});
```

--------------------------------

### SDIFFSTORE Command

Source: https://upstash.com/docs/redis/sdks/ts/commands/set/sdiffstore

The SDIFFSTORE command computes the difference between multiple sets and stores the result in a new set. It takes the destination key and the keys of the source sets as arguments.

```APIDOC
## SDIFFSTORE

### Description
Write the difference between sets to a new set.

### Method
POST

### Endpoint
/websites/upstash-redis

### Parameters
#### Request Body
- **destination** (string) - Required - The key of the set to store the resulting set in.
- **keys** (...string[]) - Required - The keys of the sets to perform the difference operation on.

### Request Example
```json
{
  "command": "sdiffstore",
  "args": ["dest", "set1", "set2"]
}
```

### Response
#### Success Response (200)
- **TValue[]** (array) - The members of the resulting set.

#### Response Example
```json
["a", "b"]
```
```

--------------------------------

### Execute Basic Redis Command via REST API (cURL)

Source: https://upstash.com/docs/redis/features/restapi

Demonstrates how to execute a basic Redis SET command using cURL. It requires the REST URL and an authorization token. The response is a JSON object containing the result.

```shell
curl https://us1-merry-cat-32748.upstash.io/set/foo/bar \
 -H "Authorization: Bearer 2553feg6a2d9842h2a0gcdb5f8efe9934"
```

--------------------------------

### Build Azure Functions Application

Source: https://upstash.com/docs/redis/quickstarts/azure-functions

Compiles and prepares the TypeScript code for deployment using the `build` script defined in your `package.json`. This typically involves transpiling TypeScript to JavaScript.

```shell
npm run build
```

--------------------------------

### Python: GETSET Command in Upstash Redis

Source: https://upstash.com/docs/redis/sdks/py/commands/string/getset

This Python code snippet demonstrates how to use the GETSET command with Upstash Redis. It first sets an initial value for a key and then uses GETSET to retrieve that old value while simultaneously setting a new one. This operation is atomic. Dependencies include the 'redis' library.

```python
redis.set("key", "old-value")

assert redis.getset("key", "newvalue") == "old-value"
```

--------------------------------

### Push Elements to List Head with Redis LPUSH (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/list/lpush

Demonstrates how to use the LPUSH command in TypeScript to add elements to the head of a list. This function requires a Redis client instance and takes the key and one or more elements as arguments. It returns the updated list length.

```typescript
const length1 = await redis.lpush("key", "a", "b", "c"); 
console.log(length1); // 3
const length2 = await redis.lpush("key", "d"); 
console.log(length2); // 4
```

--------------------------------

### KEYS API

Source: https://upstash.com/docs/redis/sdks/py/commands/generic/keys

Retrieves all keys matching a specified glob-style pattern. Use with caution in production environments.

```APIDOC
## GET /keys

### Description
Returns all keys matching a glob-style pattern. This command can block the database for a long time depending on its size and is not recommended for production use. Use SCAN instead.

### Method
GET

### Endpoint
/keys

### Parameters
#### Query Parameters
- **match** (str) - Required - A glob-style pattern. Use `*` to match all keys.

### Request Example
```json
{
  "match": "prefix*"
}
```

### Response
#### Success Response (200)
- **keys** (List[str]) - An array of keys matching the pattern.

#### Response Example
```json
{
  "keys": ["key1", "key2", "key3"]
}
```
```

--------------------------------

### Test FastAPI Session Management with Requests

Source: https://upstash.com/docs/redis/tutorials/python_session

A Python script using the `requests` library to test the FastAPI application's session management endpoints. It simulates user login, profile access, and logout by sending HTTP requests and printing the responses.

```python
import requests

base_url = "http://127.0.0.1:8000"

# Test login
response = requests.post(f"{base_url}/login/", json={"username": "abdullah"})
print("Login Response:", response.json())

# In the browser, you don't need to set cookies manually. The browser will handle it automatically.
session_cookie = response.cookies.get("session_id")

# Test profile
profile_response = requests.get(f"{base_url}/profile/", cookies={"session_id": session_cookie})
print("Access Profile Response:", profile_response.json())

# Test logout
logout_response = requests.post(f"{base_url}/logout/", cookies={"session_id": session_cookie})
print("Logout Response:", logout_response.json())

# Test profile after logout
profile_after_logout_response = requests.get(f"{base_url}/profile/", cookies={"session_id": session_cookie})
print("Access Profile After Logout Response:", profile_after_logout_response.text)

```

--------------------------------

### Monitor Redis Requests with ioredis

Source: https://upstash.com/docs/redis/howto/monitoryourusage

This snippet demonstrates how to use the `monitor` command with `ioredis` to capture and log all requests processed by an Upstash Redis instance in real-time. It requires an active Redis connection and uses an event handler to process incoming commands. Note that the `MONITOR` command does not work over HTTP and requires a persistent connection.

```typescript
const monitor = await redis.monitor()

monitor.on("monitor", (time, args, source, database) => {
  console.log(time, args, source, database)
})
```

--------------------------------

### Django View with Upstash Redis Integration

Source: https://upstash.com/docs/redis/quickstarts/vercel-python-runtime

Implements a Django view that uses the `upstash-redis` library to increment a counter stored in Redis. It initializes the Redis client from environment variables and returns an HTML response displaying the counter value.

```python
from datetime import datetime

from django.http import HttpResponse

from upstash_redis import Redis

redis = Redis.from_env()

def index(request):
    count = redis.incr('counter')
    html = f'''
    <html>
        <body>
            <h1>Counter: { count }</h1p>
        </body>
    </html>
    '''
    return HttpResponse(html)
```

--------------------------------

### SUNIONSTORE

Source: https://upstash.com/docs/redis/sdks/ts/commands/set/sunionstore

Stores the union of sets in a destination key. It takes the destination key as the first argument, followed by the keys of the sets to be unioned.

```APIDOC
## SUNIONSTORE

### Description
Returns the union between sets and stores the resulting set in a key.

### Method
POST

### Endpoint
/websites/upstash-redis

### Parameters
#### Path Parameters
None

#### Query Parameters
None

#### Request Body
- **destination** (string) - Required - The key of the set to store the resulting set in.
- **keys** (...string[]) - Required - The keys of the sets to perform the union operation on.

### Request Example
```json
{
  "command": "SUNIONSTORE",
  "args": ["destination", "set1", "set2"]
}
```

### Response
#### Success Response (200)
- **members** (TValue[]) - The members of the resulting set.

#### Response Example
```json
["a", "b", "c", "d", "e"]
```
```

--------------------------------

### Monitor All Commands with Upstash Redis (CLI)

Source: https://context7.com/context7/upstash-redis/llms.txt

This CLI command enables monitoring of all commands executed against your Upstash Redis instance. It requires a POST request to the monitor endpoint with the authorization header and the 'text/event-stream' accept header. The output provides a real-time stream of commands and their details.

```bash
curl -X POST https://us1-merry-cat-32748.upstash.io/monitor \
  -H "Authorization: Bearer 2553feg6a2d9842h2a0gcdb5f8efe9934" \
  -H "Accept: text/event-stream"
```

--------------------------------

### Set Upstash Redis Environment Variables

Source: https://upstash.com/docs/redis/integrations/celery

Exports Upstash Redis connection details as environment variables. These variables are used by Celery to establish a connection to the Redis instance. Ensure you replace placeholders with your actual credentials.

```bash
export UPSTASH_REDIS_HOST=<YOUR_HOST>
export UPSTASH_REDIS_PORT=<YOUR_PORT>
export UPSTASH_REDIS_PASSWORD=<YOUR_PASSWORD>
```

--------------------------------

### Pipeline Commands with Upstash Redis TypeScript SDK

Source: https://upstash.com/docs/redis/sdks/ts/pipelining/pipeline-transaction

Demonstrates how to use the pipeline feature in the Upstash Redis TypeScript SDK. Pipelines send multiple commands in a single HTTP request, improving efficiency. Note that pipeline execution is not atomic. Dependencies include the `@upstash/redis` package. It takes Redis connection options and returns an array of command responses.

```typescript
import { Redis } from "@upstash/redis";

const redis = new Redis({
  /* auth */
});

const p = redis.pipeline();

// Now you can chain multiple commands to create your pipeline:
p.set("key", 2);
p.incr("key");

// or inline:
p.hset("key2", "field", { hello: "world" }).hvals("key2");

// Execute the pipeline once you are done building it:
// `exec` returns an array where each element represents the response of a command in the pipeline.
// You can optionally provide a type like this to get a typed response.
const res = await p.exec<[Type1, Type2, Type3]>();
```

--------------------------------

### Expected Test Output for Session Management

Source: https://upstash.com/docs/redis/tutorials/python_session

Illustrates the expected output when running the `test_script.py`. It shows the responses from the login, profile access, and logout endpoints, including session data and error messages after logout.

```plaintext
Login Response: {'message': 'Logged in successfully', 'session_id': '68223c50-ede4-48eb-9d26-4a4dd735c10d'}
Access Profile Response: {'session_id': '68223c50-ede4-48eb-9d26-4a4dd735c10d', 'session_data': {'user': 'abdullah', 'status': 'active'}}
Logout Response: {'message': 'Logged out successfully'}
Access Profile After Logout Response: {"detail":"Session not found or expired"}
```

--------------------------------

### Docker Ignore File

Source: https://upstash.com/docs/redis/quickstarts/koyeb

Specifies intentionally untracked files that should be excluded from the Docker image build context. This helps keep Docker images small and secure.

```dockerignore
Dockerfile
.dockerignore
.git
node_modules
npm-debug.log
/.cache
.env
README.md
```

--------------------------------

### LPUSH

Source: https://upstash.com/docs/redis/sdks/py/commands/list/lpush

Pushes one or more elements to the head of a list in Upstash Redis.

```APIDOC
## LPUSH

### Description
Push an element at the head of the list.

### Method
POST

### Endpoint
/websites/upstash-redis

### Parameters
#### Request Body
- **key** (str) - Required - The key of the list.
- **elements** (*List[Any]) - Required - One or more elements to push at the head of the list.

### Response
#### Success Response (200)
- **response** (int) - Required - The length of the list after the push operation.

### Request Example
```py
{
  "key": "mylist",
  "elements": ["one", "two", "three"]
}
```

### Response Example
```json
{
  "response": 3
}
```
```

--------------------------------

### Pipelining

Source: https://upstash.com/docs/redis/features/restapi

This section explains how to use the `/pipeline` endpoint to send multiple Redis commands in a single HTTP request for improved throughput. Responses are returned as a JSON array.

```APIDOC
## Pipelining

Upstash REST API provides support for command pipelining, allowing you to send multiple commands as a batch instead of sending them individually and waiting for responses. With the pipeline API, you can include several commands in a single HTTP request, and the response will be a JSON array. Each item in the response array corresponds to the result of a command in the same order as they were included in the pipeline.

API endpoint for command pipelining is `/pipeline`. Pipelined commands should be send as a two dimensional JSON array in the request body, each row containing name of the command and its arguments.

### Request Syntax

```shell
curl -X POST https://us1-merry-cat-32748.upstash.io/pipeline \
 -H "Authorization: Bearer $TOKEN" \
 -d '
    [
      ["CMD_A", "arg0", "arg1", ..., "argN"],
      ["CMD_B", "arg0", "arg1", ..., "argM"],
      ...
    ]
    '
```

### Response Syntax

```json
[
  {"result": "RESPONSE_A"},
  {"result": "RESPONSE_B"},
  {"error": "ERR ..."}, 
  ...
]
```

<Note>
  Execution of the pipeline is *not atomic*. Even though each command in the pipeline will be executed in order, commands sent by other clients can interleave with the pipeline. Use [transactions](#transactions) API instead if you need atomicity.
</Note>

### Example Request

To send the following Redis commands using pipeline:

```redis
SET key1 valuex
SETEX key2 13 valuez
INCR key1
ZADD myset 11 item1 22 item2
```

Use the following `curl` command:

```shell
curl -X POST https://us1-merry-cat-32748.upstash.io/pipeline \
 -H "Authorization: Bearer 2553feg6a2d9842h2a0gcdb5f8efe9934" \
 -d '
    [
      ["SET", "key1", "valuex"],
      ["SETEX", "key2", 13, "valuez"],
      ["INCR", "key1"],
      ["ZADD", "myset", 11, "item1", 22, "item2"]
    ]
    '
```

### Example Response

The pipeline response will be:

```json
[
  { "result": "OK" },
  { "result": "OK" },
  { "error": "ERR value is not an int or out of range" },
  { "result": 2 }
]
```

### When to Use Pipelining

You can use pipelining when:

*   You need more throughput, since pipelining saves from multiple round-trip times. (*But beware that latency of each command in the pipeline will be equal to the total latency of the whole pipeline.*)
*   Your commands are independent of each other, meaning the response of a former command is not needed to submit a subsequent command.
```

--------------------------------

### SCAN Command

Source: https://upstash.com/docs/redis/sdks/ts/commands/generic/scan

Scans the database for keys based on provided cursor and options.

```APIDOC
## SCAN

### Description
Scan the database for keys.

### Method
GET (or POST depending on implementation)

### Endpoint
/websites/upstash-redis/scan

### Parameters
#### Query Parameters
- **cursor** (string) - Required - The cursor value. Start with "0" on the first call, then use the cursor returned by each call for the next. It's a string to safely support large numbers that might exceed JavaScript's number limits.
- **match** (string) - Optional - Glob-style pattern to filter by field names.
- **count** (number) - Optional - Number of fields to return per call.
- **type** (string) - Optional - Filter by type. For example `string`, `hash`, `set`, `zset`, `list`, `stream`.

### Request Example
```json
{
  "cursor": "0",
  "match": "*",
  "count": 10,
  "type": "string"
}
```

### Response
#### Success Response (200)
- **[string, string[]]** - The returned cursor and a list of matching keys. When the returned cursor is "0", the scan is complete.

#### Response Example
```json
{
  "cursor": "15",
  "keys": ["key1", "key2", "key3"]
}
```
```

--------------------------------

### Fetch and Display Notifications with React and Upstash Redis

Source: https://upstash.com/docs/redis/tutorials/notification

This JavaScript code snippet fetches new notification messages from Upstash Redis based on the locally stored version. It uses the `react-toastify` library to display notifications and `localStorage` to persist the notification version. Replace placeholder URLs and tokens with actual Upstash Redis REST API credentials.

```javascript
import logo from "./logo.svg";
import "./App.css";
import { toast, ToastContainer } from "react-toastify";
import "react-toastify/dist/ReactToastify.css";
import { useEffect } from "react";

function App() {
  useEffect(() => {
    async function fetchData() {
      try {
        let version = localStorage.getItem("notification-version");
        version = version ? version : 0;
        const response = await fetch(
          "REPLACE_UPSTASH_REDIS_REST_URL/zrevrangebyscore/messages/+inf/" +
            version +
            "/WITHSCORES/LIMIT/0/1",
          {
            headers: {
              Authorization: "Bearer REPLACE_UPSTASH_REDIS_REST_TOKEN",
            },
          }
        );
        const res = await response.json();
        const v = parseInt(res.result[1]);
        if (v) {
          localStorage.setItem("notification-version", v + 1);
        }
        toast(res.result[0]);
      } catch (e) {
        console.error(e);
      }
    }
    fetchData();
  });

  return (
    <div className="App">
      <header className="App-header">
        <img src={logo} className="App-logo" alt="logo" />
        <p>
          Edit <code>src/App.js</code> and save to reload.
        </p>
        <a
          className="App-link"
          href="https://reactjs.org"
          target="_blank"
          rel="noopener noreferrer"
        >
          Learn React
        </a>
      </header>
      <ToastContainer />
    </div>
  );
}

export default App;

```

--------------------------------

### HSET Command - Set Multiple Fields (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/hash/hset

This snippet illustrates setting multiple fields in a hash using the HSET command. It takes the Redis client, the hash key, and a dictionary containing multiple field-value pairs. The function returns an integer indicating how many fields were added.

```python
assert redis.hset("myhash", values={
    "field1": "Hello",
    "field2": "World"
  }) == 2
```

--------------------------------

### LPUSH Command

Source: https://upstash.com/docs/redis/sdks/ts/commands/list/lpush

The LPUSH command in Upstash Redis allows you to insert one or more elements at the beginning (head) of a list associated with a given key.

```APIDOC
## LPUSH

### Description
Push an element at the head of the list.

### Method
POST

### Endpoint
/websites/upstash-redis

### Parameters
#### Request Body
- **key** (string) - Required - The key of the list.
- **elements** (...TValue[]) - Required - One or more elements to push at the head of the list.

### Request Example
```ts
const length1 = await redis.lpush("key", "a", "b", "c"); 
console.log(length1); // 3
const length2 = await redis.lpush("key", "d"); 
console.log(length2); // 4
```

### Response
#### Success Response (200)
- **length** (number) - The length of the list after the push operation.

#### Response Example
```json
4
```
```

--------------------------------

### Implement Redis Pipelines

Source: https://upstash.com/docs/redis/sdks/py/features

Illustrates how to use pipelines to send multiple commands to Redis in a single roundtrip. This is useful for reducing latency. Commands are added to a pipeline object and then executed using `exec()`.

```python
pipeline = redis.pipeline()

pipeline.set("foo", 1)
pipeline.incr("foo")
pipeline.get("foo")

result = pipeline.exec()

print(result)
# prints [True, 2, '2']
```

```python
pipeline = redis.pipeline()

pipeline.set("foo", 1).incr("foo").get("foo")
result = pipeline.exec()

print(result)
# prints [True, 2, '2']
```

--------------------------------

### Redis LPOS With Count

Source: https://upstash.com/docs/redis/sdks/py/commands/list/lpos

Illustrates the LPOS command's `count` option, which allows retrieval of multiple indexes for a given element if it appears more than once. The result is returned as a list of indexes.

```python
redis.rpush("key", "a", "b", "b")

assert redis.lpos("key", "b", count=2) == [1, 2]
```

--------------------------------

### Fetch Weather Data with Cache Check (Elixir)

Source: https://upstash.com/docs/redis/quickstarts/elixir

This function first attempts to retrieve weather data from the cache. If not found in the cache, it proceeds to fetch the data from the external API. It handles different cache lookup results and potential errors.

```elixir
defp fetch_weather(location) do
    location = String.replace(location, " ", "%20")
    case fetch_weather_from_cache(location) do
      {:ok, cached_weather} ->
        {:ok, cached_weather}
      {:error, :not_found} ->
        fetch_weather_from_api(location)
      {:error, reason} ->
        {:error, reason}
    end
  end
```

--------------------------------

### Delete Koyeb App via CLI

Source: https://upstash.com/docs/redis/quickstarts/koyeb

Command to delete a Koyeb application and its associated service from the Koyeb platform. This is a destructive operation.

```bash
koyeb app delete example-koyeb-upstash
```

--------------------------------

### JSON.MSET

Source: https://upstash.com/docs/redis/sdks/ts/commands/json/mset

Sets multiple JSON values at multiple paths in multiple keys using the JSON.MSET command.

```APIDOC
## JSON.MSET

### Description
Sets multiple JSON values at multiple paths in multiple keys.

### Method
Generally, commands like this are executed via a client library. The underlying Redis command is JSON.MSET.

### Endpoint
N/A (Command executed via client library)

### Parameters
#### Request Body (Conceptual, as executed via client)
- **params** (object[]) - Required - A list of objects where each object contains a key, a path, and a value. Type of value can be `Array<number>`, `string`, `boolean`, `Record<string, any>`, or `Array<any>`.
  - **key** (string) - Required - The key where the JSON value will be set.
  - **path** (string) - Required - The JSON path within the key.
  - **value** (any) - Required - The JSON value to set.

### Request Example
```py
await redis.json.mset([
  { key: key, path: "$.path", value: value},
  { key: key2, path: "$.path2", value: value2}
])
```

### Response
#### Success Response (200)
- **status** (string) - Returns "OK" if the command was successful.

#### Response Example
```json
"OK"
```
```

--------------------------------

### ZINTERSTORE with Simple Intersection (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/zset/zinterstore

Demonstrates the basic usage of the ZINTERSTORE command to find the intersection of two sorted sets and store the result in a destination key. It requires adding elements to the source keys first. The output is the count of elements in the resulting intersection.

```typescript
await redis.zadd(
    "key1", 
    { score: 1, member: "member1" },
)
await redis.zadd(
    "key2",
    { score: 1, member: "member1" },
    { score: 2, member: "member2" },
)

const res = await redis.zinterstore("destination", 2, ["key1", "key2"]);
console.log(res) // 1
```

--------------------------------

### Auto-Pipelining in Action with Async Calls and Promise.all

Source: https://upstash.com/docs/redis/sdks/ts/pipelining/auto-pipeline

Illustrates how auto-pipelining works with asynchronous operations. Commands like `hincrby` are added to a pipeline and executed together when `await` is called on a `Promise.all` that includes them. This reduces the number of network requests.

```typescript
import { Redis } from "@upstash/redis";

const redis = Redis.fromEnv({
  latencyLogging: false,
  enableAutoPipelining: true
});

// async call to redis. Not executed right away, instead
// added to the pipeline
redis.hincrby("Brooklyn", "visited", 1);

// making requests in batches
const brooklynInfo = Promise.all([
  redis.hget("Brooklyn", "coordinates"),
  redis.hget("Brooklyn", "population")
]);

// when we call await, the three commands are executed
// as a pipeline automatically. A single PIPELINE command
// is executed instead of three requests and the results
// are returned:
const [ coordinates, population ] = await brooklynInfo;
```

--------------------------------

### Publish to a Channel with Upstash Redis (CLI)

Source: https://context7.com/context7/upstash-redis/llms.txt

This CLI command demonstrates how to publish a message to a specific channel in Upstash Redis. It uses a POST request to the publish endpoint, specifying the channel and the message content in the URL path, along with the necessary authorization header.

```bash
curl -X POST https://us1-merry-cat-32748.upstash.io/publish/chat/hello \
  -H "Authorization: Bearer 2553feg6a2d9842h2a0gcdb5f8efe9934"
```

--------------------------------

### API Endpoint for Redis Counter

Source: https://upstash.com/docs/redis/quickstarts/sst-v2

This is a Next.js API route (`pages/api/hello.ts`) that utilizes the `@upstash/redis` package. It initializes a Redis client using the secrets bound in the SST stack and increments a counter stored in Redis. The current count is then returned in the JSON response.

```typescript
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

--------------------------------

### Set Multiple Keys Conditionally with MSETNX in TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/string/msetnx

This snippet demonstrates how to use the MSETNX command to set multiple key-value pairs in Upstash Redis. It takes an object where keys and values are provided. The command returns true if all keys were successfully set (meaning none existed prior), and false otherwise. This is useful for ensuring that a set of keys is created atomically without overwriting existing data.

```typescript
redis.msetnx({
  "key1": "value1",
  "key2": "value2"
})
```

--------------------------------

### Implement Stale-While-Revalidate Caching with `Cache::flexible` (PHP)

Source: https://upstash.com/docs/redis/tutorials/laravel_caching

Demonstrates the use of `Cache::flexible` to implement the stale-while-revalidate caching pattern. This strategy serves stale data immediately while refreshing the cache in the background, improving performance and data freshness. It takes a cache key, an array defining fresh and stale periods, and a closure to fetch fresh data.

```php
$value = Cache::flexible('todos', [5, 10], function () {
    return Todo::all();
});
```

```php
return Cache::flexible(self::CACHE_KEY, self::CACHE_TTL, function () {
    return Todo::all();
});
```

```php
return Cache::flexible("todo.{$todo->id}",
    self::CACHE_TTL,
    function () use ($todo) {
        return $todo;
    }
);
```

--------------------------------

### Block Until Ready with Upstash Redis Rate Limiter

Source: https://upstash.com/docs/redis/sdks/ratelimit-py/features

Demonstrates how to use the `block_until_ready` method to wait for a rate limit to become available within a specified timeout. This is useful when you need to ensure a request can eventually be processed even if the immediate limit is exceeded. It requires `upstash_ratelimit` and `upstash_redis` libraries.

```python
from upstash_ratelimit import Ratelimit, SlidingWindow
from upstash_redis import Redis

# Create a new ratelimiter, that allows 10 requests per 10 seconds
ratelimit = Ratelimit(
    redis=Redis.from_env(),
    limiter=SlidingWindow(max_requests=10, window=10),
)

response = ratelimit.block_until_ready("id", timeout=30)

if not response.allowed:
    print("Unable to process, even after 30 seconds")
else:
    do_expensive_calculation()
    print("Here you go!")
```

--------------------------------

### Retrieve List Element by Index with Upstash Redis (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/list/lindex

This snippet demonstrates how to use the LINDEX command with Upstash Redis to retrieve a specific element from a list stored at a given key. It requires the `redis` client instance and specifies the key and the zero-based index of the element to fetch. If the index is out of bounds, null is returned.

```typescript
await redis.rpush("key", "a", "b", "c");
const element = await redis.lindex("key", 0);
console.log(element); // "a"
```

--------------------------------

### Verify QStash Message Signature using Receiver (TypeScript)

Source: https://upstash.com/docs/redis/howto/vercelintegration

Verify the signature and body of an incoming QStash message using the Upstash QStash receiver. Requires QSTASH_CURRENT_SIGNING_KEY and QSTASH_NEXT_SIGNING_KEY environment variables. Returns a boolean indicating validity.

```typescript
import { Receiver } from "@upstash/qstash";

const receiver = new Receiver({
  currentSigningKey: process.env.QSTASH_CURRENT_SIGNING_KEY,
  nextSigningKey: process.env.QSTASH_NEXT_SIGNING_KEY,
});

const isValid = await receiver.verify({
  signature: "..."
  body: "..."
})
```

--------------------------------

### Establish Fly.io Redis Tunnel (Shell)

Source: https://upstash.com/docs/redis/quickstarts/fly

This command initiates a secure tunnel between your local machine and the Redis instance hosted on Fly.io. It maps a local port to the remote Redis port, allowing local connections as if Redis were running on `localhost`.

```shell
fly redis connect
```

--------------------------------

### JSON.ARRINSERT

Source: https://upstash.com/docs/redis/sdks/py/commands/json/arrinsert

Inserts JSON values into an array at a specified path and index.

```APIDOC
## JSON.ARRINSERT

### Description
Inserts the JSON values into the array at the specified path before the given index. Existing elements are shifted to the right.

### Method
NATIVE_REDIS_COMMAND

### Endpoint
/websites/upstash-redis

### Parameters
#### Path Parameters
- **key** (str) - Required - The key of the JSON entry.
- **path** (str) - Required - The JSONPath expression for the array.
- **index** (int) - Required - The index at which to insert the values. Elements at this index and after will be shifted.
- **values** (...TValue[]) - Required - One or more values to insert into the array.

### Request Example
```py
length = redis.json.arrinsert("key", "$.path.to.array", 2, "a", "b")
```

### Response
#### Success Response (200)
- **length** (List[int]) - The length of the array after the insertion.

#### Response Example
```json
[2]
```
```

--------------------------------

### HSCAN Basic Usage in TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/hash/hscan

Demonstrates the basic usage of the HSCAN command to retrieve all fields and values from a hash. It first sets fields using hset and then calls hscan with a cursor of 0. The output shows the new cursor and the field-value pairs.

```typescript
await redis.hset("key", {
    id: 1,
    username: "chronark",
    name: "andreas"
   });
  const [newCursor, fields] = await redis.hscan("key", 0);
  console.log(newCursor); // likely `0` since this is a very small hash
  console.log(fields); // ["id", 1, "username", "chronark", "name", "andreas"]
```

--------------------------------

### AWS CDK Stack for Lambda Function and URL

Source: https://upstash.com/docs/redis/quickstarts/aws-lambda

Sets up the AWS CDK stack to define and deploy an AWS Lambda function. It configures the function with the TypeScript entry point, handler, runtime, and environment variables for Upstash Redis. It also adds a function URL for easy access.

```typescript
import * as cdk from 'aws-cdk-lib';
import { Construct } from 'constructs';
import * as lambda from 'aws-cdk-lib/aws-lambda';
import * as nodejs from 'aws-cdk-lib/aws-lambda-nodejs';

export class CounterCdkStack extends cdk.Stack {
  constructor(scope: Construct, id: string, props?: cdk.StackProps) {
    super(scope, id, props);

    const counterFunction = new nodejs.NodejsFunction(this, 'CounterFunction', {
      entry: 'api/counter.ts',
      handler: 'handler',
      runtime: lambda.Runtime.NODEJS_20_X,
      environment: {
        UPSTASH_REDIS_REST_URL: process.env.UPSTASH_REDIS_REST_URL || '',
        UPSTASH_REDIS_REST_TOKEN: process.env.UPSTASH_REDIS_REST_TOKEN || '',
      },
      bundling: {
        format: nodejs.OutputFormat.ESM,
        target: "node20",
        nodeModules: ['@upstash/redis'],
      },
    });

    const counterFunctionUrl = counterFunction.addFunctionUrl({
      authType: lambda.FunctionUrlAuthType.NONE,
    });

    new cdk.CfnOutput(this, "counterFunctionUrlOutput", {
      value: counterFunctionUrl.url,
    })
  }
}
```

--------------------------------

### JSON.MSET

Source: https://upstash.com/docs/redis/sdks/py/commands/json/mset

Sets multiple JSON values at multiple paths in multiple keys using the JSON.MSET command.

```APIDOC
## JSON.MSET

### Description
Sets multiple JSON values at multiple paths in multiple keys.

### Method
Not Applicable (This is a Redis command, not a REST API endpoint)

### Endpoint
Not Applicable

### Parameters
#### Body Parameters
- **key_path_value_tuples** (List[Tuple[string, string, TValue]]) - Required - A list of tuples where each tuple contains a key, a path, and a value.

### Request Example
```py
redis.json.mset([(key, "$.path", value), (key2, "$.path2", value2)])
```

### Response
#### Success Response (true)
- **true** (boolean) - Returns true if the operation was successful.

#### Response Example
```json
true
```
```

--------------------------------

### Redis ZINTER Intersection of Sets (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/zset/zunion

Demonstrates how to find the intersection of two sorted sets ('key1' and 'key2') using the ZINTER command in Python. It assumes the existence of a 'redis' client object. The output is a list of elements common to both sets.

```python
redis.zadd("key1", {"a": 1, "b": 2, "c": 3})

redis.zadd("key2", {"c": 3, "d": 4, "e": 5})

result = redis.zunion(["key1", "key2"])

assert result == ["a", "b", "c", "d", "e"]
```

--------------------------------

### Run Database Migrations

Source: https://upstash.com/docs/redis/tutorials/laravel_caching

Executes all pending database migrations, including the 'create_todos_table' migration, to apply the defined schema changes to your database.

```shell
php artisan migrate
```

--------------------------------

### Flask-SocketIO Chat Server with Upstash Redis (Python)

Source: https://upstash.com/docs/redis/tutorials/python_realtime_chat

Implements a real-time chat application using Flask and Flask-SocketIO, with Upstash Redis configured as the message queue for broadcasting messages. It handles client connections, disconnections, and message broadcasting, ensuring real-time updates across all connected clients.

```python
from flask import Flask, render_template
from flask_socketio import SocketIO
import os

# Initialize Flask app
app = Flask(__name__)
app.config["SECRET_KEY"] = os.getenv("SECRET_KEY", os.urandom(24))

# Set up Redis URL with TLS
redis_password = os.getenv('UPSTASH_REDIS_PASSWORD')
redis_host = os.getenv('UPSTASH_REDIS_HOST')
redis_port = int(os.getenv('UPSTASH_REDIS_PORT', 6379))
redis_url = f"rediss://:{redis_password}@{redis_host}:{redis_port}"

# Initialize SocketIO with Redis message queue
socketio = SocketIO(app, message_queue=redis_url, cors_allowed_origins="*")

# WebSocket handlers
@socketio.on("connect")
def handle_connect():
    print("Client connected.")

@socketio.on("disconnect")
def handle_disconnect():
    print("Client disconnected.")

@socketio.on("message")
def handle_message(data):
    """Handle incoming chat messages."""
    print(f"Message received: {data}")
    # Broadcast the message to all connected clients except the sender
    socketio.emit("message", data, include_self=False)

# Serve the chat HTML page
@app.route("/")
def index():
    return render_template("chat.html")  # Render the chat interface template

if __name__ == "__main__":
    socketio.run(app, debug=True, host="0.0.0.0", port=8000)
```

--------------------------------

### Pipeline Commands via REST

Source: https://context7.com/context7/upstash-redis/llms.txt

Execute multiple Redis commands in a single HTTP request using the /pipeline endpoint for improved throughput. Commands are executed in order but are not atomic.

```APIDOC
## POST /pipeline

### Description
Executes multiple Redis commands in a single HTTP request. Commands are processed sequentially but the operation is not atomic, meaning other clients can interleave operations.

### Method
POST

### Endpoint
`https://<your-domain>.upstash.io/pipeline`

### Parameters
#### Path Parameters
None

#### Query Parameters
None

#### Request Body
- **commands** (array of arrays) - Required - A JSON array where each element is a Redis command represented as an array of strings (e.g., `[["SET", "key1", "value1"], ["GET", "key1"]]`).

### Request Example
```bash
curl -X POST https://us1-merry-cat-32748.upstash.io/pipeline \
  -H "Authorization: Bearer <YOUR_TOKEN>" \
  -d '[
    ["SET", "user:count", "0"],
    ["INCR", "user:count"],
    ["SET", "user:1", "alice"],
    ["SET", "user:2", "bob"],
    ["GET", "user:count"],
    ["ZADD", "leaderboard", 100, "alice", 85, "bob"]
  ]'
```

### Response
#### Success Response (200)
- **results** (array) - An array containing the results of each command executed in the pipeline, in the order they were sent.

#### Response Example
```json
[
  {"result": "OK"},
  {"result": 1},
  {"result": "OK"},
  {"result": "OK"},
  {"result": "1"},
  {"result": 2}
]
```
```

--------------------------------

### Generate Todo Model and Associated Files

Source: https://upstash.com/docs/redis/tutorials/laravel_caching

This Artisan command scaffolds a new Eloquent model named 'Todo' and automatically generates its corresponding controller, factory, migration, and API resource files, streamlining the development process.

```shell
php artisan make:model Todo -cfmr --api
```

--------------------------------

### Set Multiple Keys with MSET in TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/string/mset

Demonstrates how to use the MSET command with the Upstash Redis client to set multiple keys and their corresponding values simultaneously. This method accepts an object where keys are the Redis keys and values can be of various types, including numbers, strings, and JSON objects.

```typescript
await redis.mset({
    key1: 1,
    key2: "hello",
    key3: { a: 1, b: "hello" },
});
```

--------------------------------

### Subscribe to a Channel with Upstash Redis (CLI)

Source: https://context7.com/context7/upstash-redis/llms.txt

This CLI command allows you to subscribe to a channel in Upstash Redis, which keeps the connection open to receive incoming messages. It requires a POST request to the subscribe endpoint with appropriate authorization and content type headers. Incoming messages are streamed as server-sent events.

```bash
curl -X POST https://us1-merry-cat-32748.upstash.io/subscribe/chat \
  -H "Authorization: Bearer 2553feg6a2d9842h2a0gcdb5f8efe9934" \
  -H "Accept: text/event-stream"
```

--------------------------------

### GETSET

Source: https://upstash.com/docs/redis/sdks/ts/commands/string/getset

Retrieves the value of a specified key and replaces it with a new value in Upstash Redis.

```APIDOC
## GETSET

### Description
Returns the value of the specified key and replaces it with a new value.

### Method
GET

### Endpoint
/websites/upstash-redis

### Parameters
#### Path Parameters
None

#### Query Parameters
None

#### Request Body
- **key** (string) - Required - The key to get.
- **newValue** (any) - Required - The new value to store.

### Request Example
```ts
const oldValue = await redis.getset("key", newValue);
```

### Response
#### Success Response (200)
- **value** (any) - The response is the value stored at the key or `null` if the key doesn't exist.

#### Response Example
```json
{
  "value": "oldValue"
}
```
```

--------------------------------

### LPUSHX

Source: https://upstash.com/docs/redis/sdks/ts/commands/list/lpushx

Pushes one or more elements to the head of a list if the list exists. If the list does not exist, no operation is performed and 0 is returned.

```APIDOC
## LPUSHX

### Description
Pushes one or more elements to the head of a list, but only if the list already exists. If the list does not exist, the command does nothing and returns 0.

### Method
`LPUSHX`

### Endpoint
`/LPUSHX`

### Parameters
#### Path Parameters
None

#### Query Parameters
None

#### Request Body
- **key** (string) - Required - The key of the list.
- **elements** (...TValue[]) - Required - One or more elements to push at the head of the list.

### Request Example
```json
{
  "key": "my_list",
  "elements": ["value1", "value2"]
}
```

### Response
#### Success Response (200)
- **length** (number) - The length of the list after the push operation. Returns 0 if the list did not exist and thus no element was pushed.

#### Response Example
```json
{
  "length": 4
}
```

#### Error Handling
- If the key does not exist, the command returns 0.
- Other potential errors related to Redis operations.
```

--------------------------------

### POST Value with Query Parameters for Additional Arguments (cURL)

Source: https://upstash.com/docs/redis/features/restapi

Shows how to send a POST request with a value in the body and additional Redis command arguments (like EX) as query parameters. This is equivalent to appending them to the URL.

```shell
curl -X POST -d '$VALUE' https://us1-merry-cat-32748.upstash.io/set/foo?EX=100 \
 -H "Authorization: Bearer 2553feg6a2d9842h2a0gcdb5f8efe9934"
```

--------------------------------

### HMGET Command Usage in Python

Source: https://upstash.com/docs/redis/sdks/py/commands/hash/hmget

This snippet demonstrates how to use the HMGET command with the Upstash Redis Python client. It first sets multiple fields in a hash using HSET and then retrieves specific fields using HMGET. Assumes 'redis' client is initialized.

```python
redis.hset("myhash", values={
    "field1": "Hello",
    "field2": "World"
})

assert redis.hmget("myhash", "field1", "field2") == ["Hello", "World"]
```

--------------------------------

### Upstash Redis API to List Features

Source: https://upstash.com/docs/redis/tutorials/roadmapvotingapp

This JavaScript API endpoint, designed for Next.js, fetches feature requests from a Redis Sorted Set named `roadmap`. It retrieves up to 100 features ordered by their scores (votes) and returns them as a JSON array. It uses the `ioredis` library for Redis interaction and requires a `REDIS_URL` environment variable.

```javascript
import { fixUrl } from "./utils";
import Redis from "ioredis";

module.exports = async (req, res) => {
  let redis = new Redis(fixUrl(process.env.REDIS_URL));
  let n = await redis.zrevrange("roadmap", 0, 100, "WITHSCORES");
  let result = [];
  for (let i = 0; i < n.length - 1; i += 2) {
    let item = {};
    item["title"] = n[i];
    item["score"] = n[i + 1];
    result.push(item);
  }

  redis.quit();

  res.json({
    body: result,
  });
};

```

--------------------------------

### FastAPI API with Upstash Redis Integration

Source: https://upstash.com/docs/redis/quickstarts/fastapi

A basic FastAPI application that uses Upstash Redis to store and increment a counter. It initializes the Redis client using environment variables and defines a root endpoint to handle increment requests.

```python
from fastapi import FastAPI

from upstash_redis import Redis

app = FastAPI()

redis = Redis.from_env()

@app.get("/")
def read_root():
    count = redis.incr('counter')
    return {"count": count}
```

--------------------------------

### Define API Routes for Todo Resource

Source: https://upstash.com/docs/redis/tutorials/laravel_caching

Registers API routes for the 'Todo' resource using Laravel's resource routing. This automatically defines routes for common CRUD operations like index, show, store, update, and destroy.

```php
<?php

use Illuminate\Support\Facades\Route;
use \App\Http\Controllers\TodoController;

Route::resource('todos', TodoController::class);

```

--------------------------------

### LPUSHX

Source: https://upstash.com/docs/redis/sdks/py/commands/list/lpushx

The LPUSHX command pushes one or more elements to the head of a list, but only if the list already exists. If the list does not exist, no operation is performed.

```APIDOC
## LPUSHX

### Description

Pushes one or more elements to the head of a list, but only if the list already exists. If the list does not exist, no operation is performed.

### Method

POST

### Endpoint

/websites/upstash-redis

### Parameters

#### Request Body

- **key** (str) - Required - The key of the list.
- **elements** (*List[str]) - Required - One or more elements to push at the head of the list.

### Request Example

```json
{
  "method": "lpushx",
  "arguments": ["mylist", "element1", "element2"]
}
```

### Response

#### Success Response (200)

- **result** (number) - The length of the list after the push operation. Returns `0` if the list did not exist and thus no element was pushed.

#### Response Example

```json
{
  "result": 3
}
```

```json
{
  "result": 0
}
```
```

--------------------------------

### Set Multiple JSON Values with Python (Upstash Redis)

Source: https://upstash.com/docs/redis/sdks/py/commands/json/mset

Demonstrates how to use the JSON.MSET command with Python to set multiple JSON values at specified paths within Redis keys. This function requires the Upstash Redis client library and takes a list of tuples, each containing a key, a JSON path, and the value to be set.

```python
redis.json.mset([(key, "$.path", value), (key2, "$.path2", value2)])
```

--------------------------------

### Fixed Window Rate Limiter (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ratelimit-ts/algorithms

Implements the Fixed Window rate limiting algorithm for Upstash Redis. This algorithm divides time into fixed durations and counts requests within each window. It's computationally cheap but can suffer from bursts at window boundaries. Usage involves initializing a Ratelimit or MultiRegionRatelimit object with the fixedWindow limiter.

```typescript
const ratelimit = new Ratelimit({
  redis: Redis.fromEnv(),
  limiter: Ratelimit.fixedWindow(10, "10 s"),
});
```

```typescript
const ratelimit = new MultiRegionRatelimit({
  redis: [
    new Redis({
      /* auth */
    }),
    new Redis({
      /* auth */
    })
  ],
  limiter: MultiRegionRatelimit.fixedWindow(10, "10 s"),
});
```

--------------------------------

### Express.js Session Storage with Node-Redis Client

Source: https://upstash.com/docs/redis/tutorials/express_session

This Node.js code configures an Express.js application to use Upstash Serverless Redis as its session store. It requires the 'express', 'redis', 'connect-redis', and 'express-session' npm packages. The configuration includes setting up the Redis client and defining session middleware to track page views.

```javascript
var express = require("express");
var parseurl = require("parseurl");
var session = require("express-session");
const redis = require("redis");

var RedisStore = require("connect-redis")(session);
var client = redis.createClient({
  // REPLACE HERE
});

var app = express();

app.use(
  session({
    store: new RedisStore({ client: client }),
    secret: "forest squirrel",
    resave: false,
    saveUninitialized: true,
  })
);

app.use(function (req, res, next) {
  if (!req.session.views) {
    req.session.views = {};
  }

  // get the url pathname
  var pathname = parseurl(req).pathname;

  // count the views
  req.session.views[pathname] = (req.session.views[pathname] || 0) + 1;
  next();
});

app.get("/foo", function (req, res, next) {
  res.send("you viewed this page " + req.session.views["/foo"] + " times");
});

app.get("/bar", function (req, res, next) {
  res.send("you viewed this page " + req.session.views["/bar"] + " times");
});

app.listen(3000, function () {
  console.log("Example app listening on port 3000!");
});

```

--------------------------------

### Rename Key in Python using Upstash Redis

Source: https://upstash.com/docs/redis/sdks/py/commands/generic/rename

This Python code snippet demonstrates how to rename a key in Upstash Redis. It first sets a key, then renames it to a new key, and asserts that the original key is gone and the new key has the correct value. It also shows how renaming a nonexistent key raises an exception.

```python
redis.set("key1", "Hello")
redis.rename("key1", "key2")

assert redis.get("key1") is None
assert redis.get("key2") == "Hello"

# Renaming a nonexistent key throws an exception
redis.rename("nonexistent", "key3")
```

--------------------------------

### Build and Deploy Cloudflare Worker with Wrangler

Source: https://upstash.com/docs/redis/tutorials/cloudflare_workers_with_redis

Builds and deploys the Cloudflare Worker application to the Cloudflare network using the Wrangler CLI. This command packages your code and uploads it to Cloudflare's global edge network, making it accessible via a public URL.

```shell
npx wrangler deploy
```

--------------------------------

### Upstash Redis REST API - Pipeline Commands (Bash)

Source: https://context7.com/context7/upstash-redis/llms.txt

Execute multiple Redis commands in a single HTTP request using the pipeline endpoint for improved throughput. Commands are sent as a JSON array and execute in order but are not atomic.

```bash
# Pipeline multiple commands (non-atomic)
curl -X POST https://us1-merry-cat-32748.upstash.io/pipeline \
  -H "Authorization: Bearer 2553feg6a2d9842h2a0gcdb5f8efe9934" \
  -d '[
    ["SET", "user:count", "0"],
    ["INCR", "user:count"],
    ["SET", "user:1", "alice"],
    ["SET", "user:2", "bob"],
    ["GET", "user:count"],
    ["ZADD", "leaderboard", 100, "alice", 85, "bob"]
  ]'

# Response: [
#   {"result":"OK"},
#   {"result":1},
#   {"result":"OK"},
#   {"result":"OK"},
#   {"result":"1"},
#   {"result":2}
# ]

# Commands execute in order but are not atomic
# Other clients can interleave operations
```

--------------------------------

### EVAL Command

Source: https://upstash.com/docs/redis/sdks/ts/commands/scripts/eval

Evaluate a Lua script server side.

```APIDOC
## EVAL

### Description
Evaluate a Lua script server side.

### Method
POST

### Endpoint
/websites/upstash-redis

### Parameters
#### Request Body
- **script** (string) - Required - The lua script to run.
- **keys** (string[]) - Required - All of the keys accessed in the script
- **args** (unknown[]) - Required - All of the arguments you passed to the script

### Request Example
```ts
const script = `
    return ARGV[1]
`
const result = await redis.eval(script, [], ["hello"]);
console.log(result) // "hello"
```

### Response
#### Success Response (200)
- **result** (any) - The result of the script.

#### Response Example
```json
"hello"
```
```

--------------------------------

### Publish Azure Functions Application

Source: https://upstash.com/docs/redis/quickstarts/azure-functions

Deploys your built Azure Functions application to the specified Function App in Azure. Replace `<APP_NAME>` with the name of your Function App.

```shell
func azure functionapp publish <APP_NAME>
```

--------------------------------

### Iterate and Retrieve All Keys with SCAN (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/generic/scan

This Python snippet demonstrates how to use the SCAN command to retrieve all keys from the Upstash Redis database. It iteratively calls the scan method, extending a results list with the keys returned in each iteration, until the cursor reaches 0, signifying the end of the scan. It requires the `redis` library.

```python
# Get all keys

cursor = 0
results = []

while True:
    cursor, keys = redis.scan(cursor, match="*")

    results.extend(keys)
    if cursor == 0:
        break

```

--------------------------------

### Retrieve Multiple Keys with MGET (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/string/mget

Demonstrates how to use the MGET command to fetch multiple keys from Redis using the Upstash client. The function returns an array of values, where null represents a missing key. Type safety can be applied to the expected return values.

```typescript
type MyType = {
    a: number;
    b: string;
}
const values = await redis.mget<MyType>("key1", "key2", "key3");
// values.length -> 3
```

--------------------------------

### Enqueue Job with Bull and Upstash Redis (JavaScript)

Source: https://upstash.com/docs/redis/tutorials/job_processing

This Node.js code snippet defines an AWS Lambda function that enqueues a job to an Upstash Redis instance using the Bull library. It configures the Redis connection and job queue settings, then adds an event to the 'employee registration' queue. Replace placeholders with your actual Redis credentials.

```javascript
var Queue = require("bull");

var settings = {
  stalledInterval: 300000, // How often check for stalled jobs (use 0 for never checking).
  guardInterval: 5000, // Poll interval for delayed jobs and added jobs.
  drainDelay: 300, // A timeout for when the queue is in drained state (empty waiting for jobs).
};

module.exports.hello = async (event) => {
  var taskQueue = new Queue(
    "employee registration",
    {
      redis: {
        port: 32016,
        host: "us1-upward-ant-32016.upstash.io",
        password: "ake4ff120d6b4216df220736be7eab087",
        tls: {},
      },
    },
    settings
  );
  await taskQueue.add({ event: event });

  // TODO save the employee record to a database
  return { message: "New employee event enqueued! 34", event };
};

```

--------------------------------

### Increment Redis Key Value (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/string/incr

Demonstrates how to use the INCR command in Python with Upstash Redis. This involves setting an initial value for a key and then incrementing it, asserting the expected result. Assumes a Redis client object is available.

```python
redis.set("key", 6)

assert redis.incr("key") == 7
```

--------------------------------

### Remove and Return Multiple Elements from List (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/list/rpop

This TypeScript snippet illustrates how to remove and return a specified number of elements from the end of a Redis list using the `rpop` command with a count. Elements 'a', 'b', and 'c' are pushed into a list keyed as 'key', and then two elements are popped. The result, an array of the popped elements, is logged to the console. The `redis` object is assumed to be an initialized Upstash Redis client.

```typescript
await redis.rpush("key", "a", "b", "c"); 
const element = await redis.rpop("key", 2);
console.log(element); // ["c", "b"]
```

--------------------------------

### Connect to Redis in Node.js Application (JavaScript)

Source: https://upstash.com/docs/redis/quickstarts/fly

This Node.js code snippet demonstrates how to configure a Redis client to connect using a local URL for development environments. It utilizes an environment variable to switch between the local tunnel and the production Redis URL.

```javascript
const redis = require("redis");

// Local Redis URL for development
const LOCAL_REDIS_URL = 'redis://localhost:10000'; // Replace with your actual local address
const REDIS_URL = process.env.NODE_ENV === 'development' ? LOCAL_REDIS_URL : process.env.REDIS_URL;

const client = redis.createClient({
    url: REDIS_URL
});

client.on("error", function(error) {
  console.error(error);
});

// Rest of your Redis-related code
```

--------------------------------

### Next.js Pages Router - Increment Counter with Upstash Redis

Source: https://upstash.com/docs/redis/quickstarts/nextjs-pages-router

Demonstrates how to use `getServerSideProps` in a Next.js Pages Router application to increment a Redis counter and display it on the home page. It initializes the Redis client using environment variables and uses the `incr` command.

```tsx
import type { InferGetServerSidePropsType, GetServerSideProps } from 'next'
import { Redis } from "@upstash/redis";

const redis = Redis.fromEnv();

export const getServerSideProps = (async () => {
  const count = await redis.incr("counter");
  return { props: { count } }
}) satisfies GetServerSideProps<{ count: number }>

export default function Home({
  count,
}: InferGetServerSidePropsType<typeof getServerSideProps>) {
  return (
    <div className="flex h-screen w-screen items-center justify-center">
      <h1 className="text-4xl font-bold">Counter: {count}</h1>
    </div>
  )
}
```

--------------------------------

### Perform Set Union with SUNION (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/set/sunion

This snippet demonstrates how to use the SUNION command in Upstash Redis to find the union of two sets. It first adds members to two separate sets ('set1' and 'set2') using SADD, and then calls SUNION with these keys. The resulting array, containing all unique members from both sets, is then logged. Ensure you have the Upstash Redis client initialized.

```typescript
await redis.sadd("set1", "a", "b", "c"); 
await redis.sadd("set2", "c", "d", "e"); 
const union =  await redis.sunion("set1", "set2");
console.log(union); // ["a", "b", "c", "d", "e"]
```

--------------------------------

### Serverless Framework Configuration (YAML)

Source: https://upstash.com/docs/redis/tutorials/rate-limiting

Configures the Serverless Framework service, specifying the AWS provider, Node.js runtime, and environment variables for Upstash Redis. It defines a single HTTP API function named 'ratelimit' that triggers the `handler.ratelimit` function.

```yaml
service: ratelimit-serverless

provider:
  name: aws
  runtime: nodejs20.x
  environment:
    UPSTASH_REDIS_REST_URL: ${env:UPSTASH_REDIS_REST_URL}
    UPSTASH_REDIS_REST_TOKEN: ${env:UPSTASH_REDIS_REST_TOKEN}

functions:
  ratelimit:
    handler: handler.ratelimit
    events:
      - httpApi:
          path: /
          method: get
```

--------------------------------

### Fetch Weather Data from API and Cache Response (Elixir)

Source: https://upstash.com/docs/redis/quickstarts/elixir

This function fetches weather data from the WeatherAPI. If the request is successful (status code 200), it parses the response, extracts relevant information, and then caches the result in Redis using `cache_weather_response`. It also handles API request errors.

```elixir
defp fetch_weather_from_api(location) do
    weather_api_key = System.get_env("WEATHER_API_KEY")
    url = "http://api.weatherapi.com/v1/current.json?key=#{weather_api_key}&q=#{location}&aqi=no"

    case HTTPoison.get(url) do
      {:ok, %{status_code: 200, body: body}} ->
        weather_info = body
                      |> Jason.decode!()
                      |> get_weather_info()

        # Cache the weather response in Redis for 8 hours
        cache_weather_response(location, Jason.encode!(weather_info))

        {:ok, weather_info}
      {:ok, %{status_code: status_code, body: body}} ->
        {:error, "#{body} (#{status_code})"}
      {:error, _reason} ->
        {:error, "Failed to fetch weather data."}
    end
  end
```

--------------------------------

### Redis KEYS Command

Source: https://upstash.com/docs/redis/sdks/ts/commands/generic/keys

Retrieves all keys from the Redis database that match a specified glob-style pattern. A warning is issued against using this command in production due to potential performance impacts, suggesting SCAN as an alternative.

```APIDOC
## GET /keys

### Description
Returns all keys matching a glob-style pattern. Use with caution in production as it can block the database.

### Method
GET

### Endpoint
/keys

### Parameters
#### Query Parameters
- **match** (string) - Required - A glob-style pattern. Use `*` to match all keys.

### Request Example
```bash
GET /keys?match=prefix*
```

### Response
#### Success Response (200)
- **keys** (string[]) - Array of keys matching the pattern.

#### Response Example
```json
{
  "keys": [
    "key1",
    "key2",
    "anotherkey"
  ]
}
```
```

--------------------------------

### AWS SAM Template Configuration for Upstash Redis

Source: https://upstash.com/docs/redis/tutorials/using_aws_sam

This YAML template defines an AWS Serverless Application Model (SAM) resource for an API Gateway endpoint triggering a Lambda function. It configures environment variables to pass Upstash Redis connection details (`UPSTASH_REDIS_REST_URL` and `UPSTASH_REDIS_REST_TOKEN`) to the Lambda function.

```yaml
AWSTemplateFormatVersion: '2010-09-09'
Transform: AWS::Serverless-2016-10-31
Description: >
  sam-app

  Sample SAM Template for sam-app

Globals:
  Function:
    Timeout: 3
    MemorySize: 128

Parameters:
  UpstashRedisRestURL:
    Type: String
  UpstashRedisRestToken:
    Type: String

Resources:
  HelloWorldFunction:
    Type: AWS::Serverless::Function
    Properties:
      CodeUri: hello_world/
      Handler: app.lambda_handler
      Runtime: python3.9
      Architectures:
        - x86_64
      Events:
        HelloWorld:
          Type: Api
          Properties:
            Path: /hello
            Method: get
      Environment:
        Variables:
          UPSTASH_REDIS_REST_URL: !Ref UpstashRedisRestURL
          UPSTASH_REDIS_REST_TOKEN: !Ref UpstashRedisRestToken

Outputs:
  HelloWorldApi:
    Description: "API Gateway endpoint URL for Prod stage for Hello World function"
    Value: !Sub "https://${ServerlessRestApi}.execute-api.${AWS::Region}.amazonaws.com/Prod/hello/"
  HelloWorldFunction:
    Description: "Hello World Lambda Function ARN"
    Value: !GetAtt HelloWorldFunction.Arn
  HelloWorldFunctionIamRole:
    Description: "Implicit IAM Role created for Hello World function"
    Value: !GetAtt HelloWorldFunctionRole.Arn

```

--------------------------------

### Configure Sidekiq Client and Server with Upstash Redis (Ruby)

Source: https://upstash.com/docs/redis/integrations/sidekiq

This Ruby code configures Sidekiq to use Upstash Redis for its connection. It sets the Redis URL from an environment variable for both the client and server configurations. It also defines a sample worker class 'EmailService' and functions for managing scheduled and asynchronous jobs.

```ruby
require "sidekiq"
require "sidekiq/api"

connection_url = ENV['UPSTASH_REDIS_LINK']

Sidekiq.configure_client do |config|
    config.redis = {url: connection_url}
end

Sidekiq.configure_server do |config|
    config.redis = {url: connection_url}
end

class EmailService
    include Sidekiq::Worker
    def perform(id, type)
        # Logic goes here. Let's assume sending email by printing to console.
        puts "Emailed to: " +  id + ": " + "'Congrats on " + type + " plan.'"
    end
end

def updateEmail(id, newType)
    jobFound = false

    a = Sidekiq::ScheduledSet.new
    a.each do |job|
        if job.args[0] == id
            job.delete
            jobFound = true
        end
    end

    if jobFound
        EmailService.perform_async(id, ("starting using our service and upgrading it to " + newType))
    else
        EmailService.perform_async(id, ("upgrading to " + newType))
    end
end

def sendEmail(id, type)
    case type
    when "free"
        # if free, delay for 10 seconds.
        EmailService.perform_in("10", id, "free")
    when "paid"
        # if paid, delay for 5 seconds.
        EmailService.perform_in("5", id, "paid")
    when "enterprise"
        # if enterprise, immediately queue.
        EmailService.perform_async(id, "enterprise")
    when "enterprise10k"
        EmailService.perform_async(id, "enterprise10k")
    else
        puts "Only plans are: `free`, `paid` and `enterprise`"
    end
end

def clearSchedules()
    Sidekiq::ScheduledSet.new.clear
    Sidekiq::Queue.new.clear
end
```

--------------------------------

### SUNION Command

Source: https://upstash.com/docs/redis/sdks/ts/commands/set/sunion

The SUNION command returns the union of multiple sets. It takes a variable number of set keys as arguments and returns all the elements that are present in any of the specified sets.

```APIDOC
## SUNION Command

### Description
Returns the union between sets. It takes the keys of the sets as input and returns the members of the resulting set containing elements from all specified sets.

### Method
POST

### Endpoint
/websites/upstash-redis

### Parameters
#### Request Body
- **command** (string) - Required - The command name, which is "SUNION".
- **keys** (string[]) - Required - The keys of the sets to perform the union operation on.

### Request Example
```json
{
  "command": "SUNION",
  "keys": ["set1", "set2"]
}
```

### Response
#### Success Response (200)
- **result** (TValue[]) - The members of the resulting set.

#### Response Example
```json
{
  "result": ["a", "b", "c", "d", "e"]
}
```
```

--------------------------------

### FastAPI Session Management with Upstash Redis

Source: https://upstash.com/docs/redis/tutorials/python_session

A Python FastAPI application demonstrating session management using Upstash Redis. It uses cookies to store session IDs and Redis to store session data with a 15-minute sliding expiration. Includes endpoints for login, profile access, and logout.

```python
from fastapi import FastAPI, Response, Cookie, HTTPException
from pydantic import BaseModel
from upstash_redis import Redis
from dotenv import load_dotenv
import uuid

# Load environment variables
load_dotenv()
redis = Redis.from_env()

app = FastAPI()

SESSION_TIMEOUT_SECONDS = 900  # 15 minutes

# Define the request body model for login
class LoginRequest(BaseModel):
    username: str

@app.post("/login/")
async def login(request: LoginRequest, response: Response):
    session_id = str(uuid.uuid4())
    redis.hset(f"session:{session_id}", values={"user": request.username, "status": "active"})
    redis.expire(f"session:{session_id}", SESSION_TIMEOUT_SECONDS)

    response.set_cookie(key="session_id", value=session_id, httponly=True)
    return {"message": "Logged in successfully", "session_id": session_id}


@app.get("/profile/")
async def get_profile(session_id: str = Cookie(None)):
    if not session_id:
        raise HTTPException(status_code=403, detail="No session cookie found")

    session_data = redis.hgetall(f"session:{session_id}")
    if not session_data:
        response = Response()
        response.delete_cookie(key="session_id") # Clear the expired cookie
        raise HTTPException(status_code=404, detail="Session expired")

    # Update the session expiration time (sliding expiration)
    redis.expire(f"session:{session_id}", SESSION_TIMEOUT_SECONDS)

    return {"session_id": session_id, "session_data": session_data}


@app.post("/logout/")
async def logout(response: Response, session_id: str = Cookie(None)):
    if session_id:
        redis.delete(f"session:{session_id}")
        response.delete_cookie(key="session_id")
    return {"message": "Logged out successfully"}

```

--------------------------------

### Token Bucket Rate Limiter (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ratelimit-ts/algorithms

Provides an implementation of the Token Bucket rate limiting algorithm for Upstash Redis. This algorithm smooths out request bursts by consuming tokens from a refilling bucket. It allows for higher initial bursts but is computationally expensive. Currently, it's not supported for `MultiRegionRatelimit`.

```typescript
const ratelimit = new Ratelimit({
  redis: Redis.fromEnv(),
  limiter: Ratelimit.tokenBucket(5, "10 s", 10),
  analytics: true,
});
```

--------------------------------

### ZINTERSTORE with Aggregation (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/zset/zinterstore

Illustrates using the ZINTERSTORE command with an aggregation method. The `aggregate` option can be set to 'sum', 'min', or 'max' to define how scores are handled when combining elements from the intersecting sets.

```typescript
await redis.zadd(
    "key1", 
    { score: 1, member: "member1" },
)
await redis.zadd(
    "key2",
    { score: 1, member: "member1" },
    { score: 2, member: "member2" },
)
const res = await redis.zinterstore(
    "destination",
    2,
    ["key1", "key2"],
    { aggregate: "sum" },
);
console.log(res) // 1
```

--------------------------------

### Upstash API Key Generation (cURL)

Source: https://upstash.com/docs/redis/help/integration

This cURL command demonstrates how to obtain a developer API key from Upstash after a successful token exchange. It requires an Authorization header with the obtained JWT key and a JSON payload specifying the key name.

```bash
curl https://api.upstash.com/apikey -H "Authorization: Bearer JWT_KEY" -d '{ "name" : "APPNAME_API_KEY_TIMESTAMP" }'
```

--------------------------------

### Todo Factory for Generating Fake Data

Source: https://upstash.com/docs/redis/tutorials/laravel_caching

This factory defines how to generate fake 'Todo' model instances. It uses the Faker library to create realistic sentence data for the 'title' field, useful for testing and development.

```php
<?php

namespace Database\Factories;

use Illuminate\Database\Eloquent\Factories\Factory;

/**
 * @extends \Illuminate\Database\Eloquent\Factories\Factory<\App\Models\Todo>
 */
class TodoFactory extends Factory
{
    /**
     * Define the model's default state.
     *
     * @return array<string, mixed>
     */
    public function definition(): array
    {
        return [
            'title' => $this->faker->sentence,
        ];
    }
}

```

--------------------------------

### Renaming a Key if it Does Not Exist (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/generic/renamenx

This TypeScript snippet demonstrates how to use the RENAMENX command with Upstash Redis. It renames the key 'old' to 'new' only if 'new' does not already exist. The result indicates whether the rename was successful.

```typescript
const renamed = await redis.renamenx("old", "new");
```

--------------------------------

### Implement Redis Transactions

Source: https://upstash.com/docs/redis/sdks/py/features

Demonstrates how to use transactions (multi) to execute a group of commands atomically. Unlike pipelines, transactions ensure that no other client can execute commands between the WATCH and EXEC calls. Commands are added and then executed using `exec()`.

```python
pipeline = redis.multi()

pipeline.set("foo", 1)
pipeline.incr("foo")
pipeline.get("foo")

result = pipeline.exec()

print(result)
# prints [True, 2, '2']
```

--------------------------------

### Set Multiple JSON Values with JSON.MSET (Python)

Source: https://upstash.com/docs/redis/sdks/ts/commands/json/mset

Demonstrates how to use the JSON.MSET command in Python to set multiple JSON values at specified paths within different keys. This function requires a list of objects, each containing a key, a JSON path, and the value to be set. The value can be of various JSON-compatible types.

```python
await redis.json.mset([
  { key: key, path: "$.path", value: value},
  { key: key2, path: "$.path2", value: value2}
])
```

--------------------------------

### Append Value to Redis String (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/string/append

Demonstrates how to use the APPEND command in Python to append a value to a string stored at a key. It checks the return value and verifies the updated string content.

```python
redis.set("key", "Hello")

assert redis.append("key", " World") == 11

assert redis.get("key") == "Hello World"
```

--------------------------------

### Enable Redis Keyspace Notifications (cURL)

Source: https://upstash.com/docs/redis/howto/keyspacenotifications

Enables keyspace notifications for hash commands using the Upstash Redis REST API via cURL. Requires a bearer token and the REST URL. This command sets the `notify-keyspace-events` configuration to 'Kh'.

```bash
curl -X POST \
    -d '["CONFIG", "SET", "notify-keyspace-events", "Kh"]' \
    -H "Authorization: Bearer $UPSTASH_REDIS_REST_TOKEN" \
    $UPSTASH_REDIS_REST_URL
```

--------------------------------

### Cloudflare Worker Fetch Handler with Upstash Redis

Source: https://upstash.com/docs/redis/tutorials/cloudflare_workers_with_redis

Implements the main fetch handler for a Cloudflare Worker using TypeScript. It initializes the Upstash Redis client from environment variables, retrieves the client's country from the request headers, and fetches a custom greeting from Redis. If no country-specific greeting is found, it defaults to 'Hello!'.

```typescript
import {
	Redis
} from '@upstash/redis/cloudflare';

type RedisEnv = {
	UPSTASH_REDIS_REST_URL: string;
	UPSTASH_REDIS_REST_TOKEN: string;
};

export default {
	async fetch(request: Request, env: RedisEnv) {
		const redis = Redis.fromEnv(env);

		const country = request.headers.get('cf-ipcountry');
		if (country) {
			const greeting = await redis.get<string>(country);
			if (greeting) {
				return new Response(greeting);
			}
		}

		return new Response('Hello!');
	},
};

```

--------------------------------

### Add Members to Sorted Set and Scan with Match and Count

Source: https://upstash.com/docs/redis/sdks/ts/commands/zset/zscan

This snippet illustrates adding members to a sorted set with ZADD and then performing a ZSCAN operation with both a match pattern and a count limit. It shows how to retrieve a specific number of members that match the pattern. Dependencies include the Upstash Redis client.

```typescript
await redis.zadd("key", 
    { score: 1, member: "a" },
    { score: 2, member: "ab" },
    { score: 3, member: "b" },
    { score: 4, member: "c" },
    { score: 5, member: "d" },
)
const [newCursor, members] = await redis.zscan("key", 0, { match: "a*", count: 1});
console.log(newCursor); // likely `0` since this is a very small set
console.log(members); // ["a"]
```

--------------------------------

### ZUNIONSTORE Command

Source: https://upstash.com/docs/redis/sdks/py/commands/zset/zunionstore

Writes the union between sets to a new key. Supports custom weights, aggregation functions, and score inclusion.

```APIDOC
## ZUNIONSTORE

### Description
Writes the union between sets to a new key.

### Method
POST

### Endpoint
/databases/{database_id}/commands/zunionstore

### Parameters
#### Path Parameters
- **database_id** (string) - Required - The ID of the database.

#### Query Parameters
- **destination** (string) - Required - The key to store the resulting set in.
- **keys** (List[string]) - Required - The keys of the sets to compare.
- **weights** (List[float]) - Optional - The weights to apply to the sets. Defaults to None.
- **aggregate** (string) - Optional - The aggregation function to apply to the sets. Allowed values: "SUM", "MIN", "MAX". Defaults to "sum".
- **withscores** (boolean) - Optional - Whether to include scores in the result. Defaults to false.

### Request Body
```json
{
  "destination": "string",
  "keys": [
    "string"
  ],
  "weights": [
    0.0
  ],
  "aggregate": "SUM" | "MIN" | "MAX",
  "withscores": true
}
```

### Request Example
```python
redis.zunionstore("destination_key", ["key1", "key2"])
redis.zunionstore("destination_key", ["key1", "key2"], weights=[2, 3], aggregate="SUM", withscores=True)
```

### Response
#### Success Response (200)
- **integer** (integer) - The number of elements in the resulting set.

#### Response Example
```json
{
  "result": 5
}
```

#### Error Response (400)
- **string** - An error message describing the issue.

#### Error Example
```json
{
  "error": "Invalid input parameters."
}
```
```

--------------------------------

### Upstash Redis LPOS Command - With Rank Option (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/list/lpos

Illustrates how to use the LPOS command with the 'rank' option in TypeScript. This allows finding the index of a specific occurrence of an element when duplicates exist in the list.

```typescript
await redis.rpush("key", "a", "b", "c", "b"); 
const index = await redis.lpos("key", "b", { rank: 2 });
console.log(index); // 3
```

--------------------------------

### POST /monitor (Monitor Command)

Source: https://upstash.com/docs/redis/features/restapi

Listen for Redis monitor events using Server-Sent Events (SSE). Incoming data will be streamed as separate 'data' lines.

```APIDOC
## POST /monitor

### Description
Listen for Redis monitor events using Server-Sent Events (SSE). Incoming data will be streamed as separate 'data' lines.

### Method
POST

### Endpoint
/monitor

### Parameters
#### Headers
- **Accept**: `text/event-stream` - Required
- **Authorization**: `Bearer <TOKEN>` - Required

### Response
#### Success Response (200)
- **data**: (string) - Each line starting with `data:` represents a monitor event.

### Response Example
```
data: "OK"
data: 1721284005.242090 [0 0.0.0.0:0] "GET" "k"
data: 1721284008.663811 [0 0.0.0.0:0] "SET" "k" "v"
```
```

--------------------------------

### Upstash Redis Integration in Lambda (Python)

Source: https://upstash.com/docs/redis/tutorials/using_aws_sam

This Python code snippet demonstrates how to initialize and use the Upstash Redis client within an AWS Lambda function. It retrieves connection details from environment variables and uses the `incr` command to increment a counter stored in Redis.

```python
from upstash_redis import Redis

redis = Redis.from_env()

def lambda_handler(event, context):
    count = redis.incr('counter')
    return {
        'statusCode': 200,
        'body': f'Counter: {count}'
    }
```

--------------------------------

### Add Members to Sorted Set and Scan with Match

Source: https://upstash.com/docs/redis/sdks/ts/commands/zset/zscan

This snippet demonstrates how to add members with scores to a sorted set using ZADD and then scan the set for members matching a pattern using ZSCAN. It shows the initial cursor and the filtered members. Dependencies include the Upstash Redis client.

```typescript
await redis.zadd("key", 
    { score: 1, member: "a" },
    { score: 2, member: "ab" },
    { score: 3, member: "b" },
    { score: 4, member: "c" },
    { score: 5, member: "d" },
)
const [newCursor, members] = await redis.zscan("key", 0, { match: "a*"});
console.log(newCursor); // likely `0` since this is a very small set
console.log(members); // ["a", "ab"]
```

--------------------------------

### Increment Redis Key Value (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/string/incrby

Demonstrates how to increment an integer value stored in a Redis key using the `incrby` command in Python. It requires a Redis client instance and sets an initial value before asserting the incremented result.

```python
redis.set("key", 6)

assert redis.incrby("key", 4) == 10
```

--------------------------------

### Redis LPOS With Rank

Source: https://upstash.com/docs/redis/sdks/py/commands/list/lpos

Shows how to use the LPOS command with the `rank` argument to find a specific occurrence of an element in a Redis list. This is useful when an element appears multiple times.

```python
redis.rpush("key", "a", "b", "c", "b"); 

assert redis.lpos("key", "b", rank=2) == 3
```

--------------------------------

### Check Redis Notification Configuration (redis-cli)

Source: https://upstash.com/docs/redis/howto/keyspacenotifications

Retrieves the current value of the `notify-keyspace-events` configuration option using redis-cli. This command connects to the Redis instance and displays the active notification settings.

```bash
redis-cli --tls -u $UPSTASH_REDIS_CLI_URL config get notify-keyspace-events
```

--------------------------------

### LRANGE

Source: https://upstash.com/docs/redis/sdks/py/commands/list/lrange

Returns the specified elements of the list stored at key.

```APIDOC
## LRANGE

### Description
Returns the specified elements of the list stored at key.

### Method
N/A (This is a command, not a REST API endpoint)

### Endpoint
N/A

### Parameters
#### Path Parameters
N/A

#### Query Parameters
N/A

#### Request Body
- **key** (str) - Required - The key of the list.
- **start** (int) - Required - The starting index of the range to return. Use negative numbers to specify offsets starting at the end of the list.
- **end** (int) - Required - The ending index of the range to return. Use negative numbers to specify offsets starting at the end of the list.

### Request Example
```py
redis.rpush("mylist", "one", "two", "three")

assert redis.lrange("mylist", 0, 1) == ["one", "two"]

assert redis.lrange("mylist", 0, -1) == ["one", "two", "three"]
```

### Response
#### Success Response (200)
- **Response** (List[str]) - The list of elements in the specified range.

#### Response Example
```json
{
  "response": ["one", "two"]
}
```
```

--------------------------------

### ZINTERSTORE

Source: https://upstash.com/docs/redis/sdks/ts/commands/zset/zinterstore

Writes the intersection between sets to a new key.

```APIDOC
## ZINTERSTORE

### Description
Writes the intersection between sets to a new key.

### Method
POST

### Endpoint
/websites/upstash-redis

### Parameters
#### Path Parameters
None

#### Query Parameters
None

#### Request Body
- **destination** (string) - Required - The key to write the intersection to.
- **keys** (integer) - Required - How many keys to compare.
- **keys** (string | string[]) - Required - The keys to compare.
- **options** (object) - Optional - Additional options for the command.
  - **aggregate** (sum | min | max) - Optional - The aggregation method.
  - **weight** (number) - Optional - The weight to apply to each key.
  - **weights** (number[]) - Optional - The weights to apply to each key.

### Request Example
```ts
// Simple Example
await redis.zadd("key1", { score: 1, member: "member1" })
await redis.zadd("key2", { score: 1, member: "member1" }, { score: 2, member: "member2" })
const res = await redis.zinterstore("destination", 2, ["key1", "key2"]);
console.log(res) // 1

// With Weights
await redis.zadd("key1", { score: 1, member: "member1" })
await redis.zadd("key2", { score: 1, member: "member1" }, { score: 2, member: "member2" })
const resWeights = await redis.zinterstore("destination", 2, ["key1", "key2"], { weights: [2, 3] });
console.log(resWeights) // 1

// Aggregate
await redis.zadd("key1", { score: 1, member: "member1" })
await redis.zadd("key2", { score: 1, member: "member1" }, { score: 2, member: "member2" })
const resAggregate = await redis.zinterstore("destination", 2, ["key1", "key2"], { aggregate: "sum" });
console.log(resAggregate) // 1
```

### Response
#### Success Response (200)
- **result** (integer) - The number of elements in the resulting set.

#### Response Example
```json
{
  "result": 1
}
```
```

--------------------------------

### TypeScript: Ratelimit Method Signature

Source: https://upstash.com/docs/redis/sdks/ratelimit-ts/methods

Defines the signature for the `limit` method in the Ratelimit library. It takes an identifier and an optional request object, returning a Promise that resolves to a `RatelimitResponse`.

```ts
ratelimit.limit(
  identifier: string,
  req?: {
    geo?: Geo;
    rate?: number,
    ip?: string,
    userAgent?: string,
    country?: string
  },
): Promise<RatelimitResponse>
```

--------------------------------

### MSET Command

Source: https://upstash.com/docs/redis/sdks/ts/commands/string/mset

Sets multiple keys in Redis using a single command. This is efficient for batch operations.

```APIDOC
## MSET

### Description
Sets multiple keys in one go. For billing purposes, this counts as a single command.

### Method
POST

### Endpoint
/websites/upstash-redis

### Parameters
#### Request Body
- **params** (Record<string, TValue>) - Required - An object where the keys are the keys to set, and the values are the values to set.

### Request Example
```json
{
  "command": "MSET",
  "args": [
    {
      "key1": 1,
      "key2": "hello",
      "key3": {"a": 1, "b": "hello"}
    }
  ]
}
```

### Response
#### Success Response (200)
- **status** (string) - 'OK' indicating the command was successful.

#### Response Example
```json
{
  "result": "OK"
}
```
```

--------------------------------

### Enable Analytics for Rate Limiting (JavaScript)

Source: https://upstash.com/docs/redis/sdks/ratelimit-ts/features

Illustrates how to enable analytics collection for the Upstash Redis Ratelimit SDK. When enabled, analytics data (hour, identifier, success/failure counts) is sent to Redis and viewable in the Upstash console. This feature can impact costs and requires careful handling in environments like Cloudflare Workers.

```javascript
const ratelimit = new Ratelimit({
  redis,
  analytics: true,
  limiter: Ratelimit.slidingWindow(60, "10s"),
});
```

--------------------------------

### Retrieve values from multiple JSON documents using Python

Source: https://upstash.com/docs/redis/sdks/py/commands/json/mget

This Python code snippet demonstrates how to use the `redis.json.mget` command to retrieve values from a specific path across multiple JSON documents. It requires the `redis` library and assumes a Redis client instance named `redis` is already configured.

```python
values = redis.json.mget(["key1", "key2"],  "$.path.to.somewhere")
```

--------------------------------

### Transaction Commands with Upstash Redis TypeScript SDK

Source: https://upstash.com/docs/redis/sdks/ts/pipelining/pipeline-transaction

Illustrates how to perform atomic operations using the transaction (multi) feature in the Upstash Redis TypeScript SDK. Transactions ensure that a group of commands execute atomically. Dependencies include the `@upstash/redis` package. It takes Redis connection options and returns an array of command responses.

```typescript
import { Redis } from "@upstash/redis";

const redis = new Redis({
  /* auth */
});

const p = redis.multi();

p.set("key", 2);
p.incr("key");

// or inline:
p.hset("key2", "field", { hello: "world" }).hvals("key2");

// execute the transaction
const res = await p.exec<[Type1, Type2, Type3]>();
```

--------------------------------

### Set Bit in Redis using Python

Source: https://upstash.com/docs/redis/sdks/py/commands/bitmap/setbit

Demonstrates how to set a specific bit at a given offset within a Redis key using the Python client. This function is useful for bit manipulation operations. It requires the `redis-py` library. The function takes the key, offset, and the bit value (0 or 1) as arguments and returns the original bit value.

```python
import redis

r = redis.Redis(host='YOUR_REDIS_HOST', port=6379, db=0)

key = "mybitset"
offset = 4
value = 1

original_bit = r.setbit(key, offset, value)
print(f"Original bit at offset {offset}: {original_bit}")
print(f"Bit set to {value} at offset {offset}.")
```

--------------------------------

### Retrieve List Elements using LRANGE in TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/list/lrange

This snippet demonstrates how to use the LRANGE command with the Upstash Redis client in TypeScript. It first pushes elements 'a', 'b', and 'c' to a list named 'key' using LPUSH, then retrieves elements from index 1 to 2 (inclusive), and finally logs the result. The 'redis' object is assumed to be an instance of the Upstash Redis client.

```typescript
await redis.lpush("key", "a", "b", "c"); 
const elements = await redis.lrange("key", 1, 2); 
console.log(elements) // ["b", "c"]
```

--------------------------------

### Upstash Redis LPOS Command - With Count Option (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/list/lpos

Shows the LPOS command usage with the 'count' option in TypeScript. This enables retrieving all occurrences of an element up to a specified limit within the Redis list.

```typescript
await redis.rpush("key", "a", "b", "b");
const positions = await redis.lpos("key", "b", { count: 2 });
console.log(positions); // [1, 2]
```

--------------------------------

### Move Element Between Lists using Python

Source: https://upstash.com/docs/redis/sdks/py/commands/list/lmove

Demonstrates how to use the LMOVE command in Python to move an element from the right side of the source list to the left side of the destination list. It initializes lists, performs the move, and asserts the results.

```python
redis.rpush("source", "one", "two", "three")
redis.lpush("destination", "four", "five", "six")

assert redis.lmove("source", "destination", "RIGHT", "LEFT") == "three"

assert redis.lrange("source", 0, -1) == ["one", "two"]
```

--------------------------------

### Next.js API Route with Redis Caching and Rate Limiting

Source: https://context7.com/context7/upstash-redis/llms.txt

This snippet demonstrates a Next.js API route using Upstash Redis for caching product data and implementing IP-based rate limiting. It fetches data from a database if not found in cache and sets an expiration time for the cache. It also handles POST requests for creating products, invalidating the cache, and updating statistics.

```typescript
import { Redis } from "@upstash/redis";
import { Ratelimit } from "@upstash/ratelimit";
import { NextRequest, NextResponse } from "next/server";

const redis = Redis.fromEnv();
const ratelimit = new Ratelimit({
  redis,
  limiter: Ratelimit.slidingWindow(10, "10 s"),
});

export async function GET(request: NextRequest) {
  // Rate limiting by IP
  const ip = request.ip || "anonymous";
  const { success, pending } = await ratelimit.limit(ip);

  if (!success) {
    return NextResponse.json(
      { error: "Too many requests" },
      { status: 429 }
    );
  }

  // Check cache
  const cacheKey = "products:all";
  let products = await redis.get(cacheKey);

  if (!products) {
    // Fetch from database
    products = await db.query("SELECT * FROM products");

    // Cache for 5 minutes
    await redis.set(cacheKey, JSON.stringify(products), { ex: 300 });
  } else {
    products = JSON.parse(products);
  }

  // Wait for analytics and multi-region sync
  await pending;

  return NextResponse.json({ products });
}

export async function POST(request: NextRequest) {
  const ip = request.ip || "anonymous";
  const { success } = await ratelimit.limit(ip);

  if (!success) {
    return NextResponse.json({ error: "Too many requests" }, { status: 429 });
  }

  const body = await request.json();

  // Save to database
  const product = await db.insert("products", body);

  // Invalidate cache
  await redis.del("products:all");

  // Update counter
  await redis.incr("stats:products:created");

  return NextResponse.json({ product }, { status: 201 });
}

```

--------------------------------

### SCAN Database Keys

Source: https://upstash.com/docs/redis/sdks/py/commands/generic/scan

Scan the database for keys using a cursor, optional match pattern, count, and type.

```APIDOC
## SCAN /websites/upstash-redis

### Description
Scan the database for keys using a cursor, optional match pattern, count, and type. This command is used to iterate over the keys in the database.

### Method
GET (or POST, depending on implementation, typically SCAN is a command not a REST endpoint)

### Endpoint
`/websites/upstash-redis` (This is a conceptual endpoint based on the project path, actual Redis SCAN is a command)

### Parameters
#### Query Parameters (Conceptual for RESTful representation)
- **cursor** (int) - Required - The cursor, use `0` in the beginning and then use the returned cursor for subsequent calls.
- **match** (str) - Required - Glob-style pattern to filter by field names.
- **count** (int) - Required - Number of fields to return per call.
- **type** (str) - Optional - Filter by type. For example `string`, `hash`, `set`, `zset`, `list`, `stream`.

### Request Example
```json
{
  "cursor": 0,
  "match": "*",
  "count": 10,
  "type": "string"
}
```

### Response
#### Success Response (200)
- **new_cursor** (int) - The new cursor for the next iteration. If `0`, the iteration is complete.
- **keys** (List[str]) - A list of keys found in the current scan.

#### Response Example
```json
{
  "new_cursor": 12345,
  "keys": ["key1", "key2", "key3"]
}
```

#### Response Example (Iteration Complete)
```json
{
  "new_cursor": 0,
  "keys": ["key4", "key5"]
}
```
```

--------------------------------

### Insert JSON values into an array with Python

Source: https://upstash.com/docs/redis/sdks/py/commands/json/arrinsert

This Python snippet demonstrates how to use the JSON.ARRINSERT command in Upstash Redis. It takes the key, path, index, and the values to insert as arguments. The command returns the new length of the array.

```python
length = redis.json.arrinsert("key", "$.path.to.array", 2, "a", "b")
```

--------------------------------

### Deno Handler Function for Upstash Redis View Counter

Source: https://upstash.com/docs/redis/quickstarts/deno-deploy

This Deno handler function uses the Upstash Redis client to increment a counter for each request. It requires UPSTASH_REDIS_REST_URL and UPSTASH_REDIS_REST_TOKEN environment variables for authentication. The function returns the current counter value in a JSON response.

```typescript
import { serve } from "https://deno.land/std@0.142.0/http/server.ts";
import { Redis } from "https://deno.land/x/upstash_redis@v1.14.0/mod.ts";

serve(async (_req: Request) => {
  if (!_req.url.endsWith("favicon.ico")) {
    const redis = new Redis({
      url: "UPSTASH_REDIS_REST_URL",
      token: "UPSTASH_REDIS_REST_TOKEN",
    });

    const counter = await redis.incr("deno-counter");
    return new Response(JSON.stringify({ counter }), { status: 200 });
  }
});
```

--------------------------------

### Create Azure Function App

Source: https://upstash.com/docs/redis/quickstarts/azure-functions

Creates an Azure Function App. This command provisions the serverless compute environment for your functions. Replace placeholders for region, app name, and storage account name. It uses Node.js v18 and Azure Functions runtime v4.

```shell
az functionapp create --resource-group AzureFunctionsQuickstart-rg --consumption-plan-location <REGION> --runtime node --runtime-version 18 --functions-version 4 --name <APP_NAME> --storage-account <STORAGE_NAME>
```

--------------------------------

### ZUNIONSTORE with Simple Union - TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/zset/zunionstore

Performs a union of two sorted sets and stores the result in a new key. It takes the destination key, the number of keys to union, and an array of source keys as arguments. The result is the number of elements in the new set.

```typescript
await redis.zadd(
    "key1", 
    { score: 1, member: "member1" },
)
await redis.zadd(
    "key2",
    { score: 1, member: "member1" },
    { score: 2, member: "member2" },
)

const res = await redis.zunionstore("destination", 2, ["key1", "key2"]);
console.log(res) // 2
```

--------------------------------

### PUBLISH

Source: https://upstash.com/docs/redis/sdks/ts/commands/pubsub/publish

Publishes a message to a specified channel in Upstash Redis.

```APIDOC
## PUBLISH

### Description
Publish a message to a channel.

### Method
POST

### Endpoint
/websites/upstash-redis

### Parameters
#### Request Body
- **channel** (string) - Required - The channel to publish to.
- **message** (TMessage) - Required - The message to publish.

### Request Example
```json
{
  "channel": "my-channel",
  "message": "my-message"
}
```

### Response
#### Success Response (200)
- **listeners** (integer) - Required - The number of clients who received the message.

#### Response Example
```json
{
  "listeners": 1
}
```
```

--------------------------------

### PSUBSCRIBE

Source: https://upstash.com/docs/redis/sdks/ts/commands/pubsub/psubscribe

Subscribe to one or more channels using a pattern matching.

```APIDOC
## PSUBSCRIBE /websites/upstash-redis

### Description
Subscribe to one or more channels using a pattern matching.

### Method
POST

### Endpoint
/websites/upstash-redis

### Parameters
#### Request Body
- **patterns** (string | string[]) - Required - The patterns matching channels to publish to.

### Request Example
```typescript
const subscription = redis.psubscribe(["user:*"]);

const messages = [];
subscription.on("pmessage", (data) => {
  messages.push(data.message);
});

await redis.publish("user:123", "user:123 message"); // receives
await redis.publish("user:456", "user:456 message"); // receives
await redis.publish("other:789", "other:789 message"); // doesn't receive

console.log(messages[0]) // user:123 message
console.log(messages[1]) // user:456 message
console.log(messages[2]) // undefined
```

### Response
#### Success Response (200)
- **subscriber** (Subscriber) - A subscriber instance which can subscribe to channels.

#### Response Example
```json
{
  "subscriber": "<subscriber_instance>"
}
```
```

--------------------------------

### Evaluate Lua Script with Upstash Redis (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/scripts/eval

Executes a Lua script server-side using the EVAL command in Upstash Redis. This function takes the Lua script as a string, an array of keys accessed by the script, and an array of arguments for the script. The result of the script execution is returned. Ensure the script and its arguments are correctly formatted.

```typescript
const script = `
      return ARGV[1]
  `
  const result = await redis.eval(script, [], ["hello"]);
  console.log(result) // "hello"
```

--------------------------------

### Remove and Return Last Element from List (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/list/rpop

This TypeScript snippet demonstrates how to use the `rpop` command to remove and return the last element from a Redis list. It first pushes elements 'a', 'b', and 'c' into a list keyed as 'key' and then pops the last element, logging it to the console. The `redis` object is assumed to be an initialized Upstash Redis client.

```typescript
await redis.rpush("key", "a", "b", "c"); 
const element = await redis.rpop("key");
console.log(element); // "c"
```

--------------------------------

### ZUNIONSTORE with Weights - TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/zset/zunionstore

Performs a union of sorted sets with specified weights applied to each source set. This allows for weighted aggregation of elements. The weights option takes an array of numbers corresponding to the source keys.

```typescript
await redis.zadd(
    "key1", 
    { score: 1, member: "member1" },
)
await redis.zadd(
    "key2",
    { score: 1, member: "member1" },
    { score: 2, member: "member2" },
)
const res = await redis.zunionstore(
    "destination",
    2,
    ["key1", "key2"],
    { weights: [2, 3] },
);
console.log(res) // 2
```

--------------------------------

### Per-Query Caching with Drizzle ORM

Source: https://upstash.com/docs/redis/integrations/drizzle

Demonstrates how to opt-in for caching a specific Drizzle ORM query using the `.$withCache()` method. This allows selective caching of query results without enabling global caching.

```typescript
await db.insert(users).value({ email: "cacheman@upstash.com" });

// 👇 reads from cache
await db.select().from(users).$withCache()
```

--------------------------------

### Configure Upstash Redis SSE MCP Server with Proxy (JSON)

Source: https://upstash.com/docs/redis/integrations/mcp

This configuration sets up an SSE MCP server for Upstash Redis, using `supergateway` as a proxy to enable client compatibility. It directs traffic to an SSE endpoint and uses OAuth2 Bearer tokens for authentication. This is designed for deployments where clients cannot directly connect to SSE servers.

```json
{
  "mcpServers": {
    "upstash": {
      "command": "npx",
      "args": [
        "-y",
        "supergateway",
        "--sse",
        "https://mcp.upstash.io/sse",
        "--oauth2Bearer",
        "<UPSTASH_EMAIL>:<UPSTASH_API_KEY>"
      ]
    }
  }
}
```

```json
{
  "servers": {
    "upstash": {
      "type": "stdio",
      "command": "npx",
      "args": [
        "-y",
        "supergateway",
        "--sse",
        "https://mcp.upstash.io/sse",
        "--oauth2Bearer",
        "<UPSTASH_EMAIL>:<UPSTASH_API_KEY>"
      ]
    }
  }
}
```

--------------------------------

### TypeScript: Ratelimit blockUntilReady Method Signature

Source: https://upstash.com/docs/redis/sdks/ratelimit-ts/methods

Defines the signature for the `blockUntilReady` method. It accepts an identifier and a timeout in milliseconds, returning a Promise that resolves to a `RatelimitResponse`.

```ts
ratelimit.blockUntilReady(
  identifier: string,
  timeout: number
): Promise<RatelimitResponse>
```

--------------------------------

### Add Feature Request to Roadmap (JavaScript)

Source: https://upstash.com/docs/redis/tutorials/roadmapvotingapp

This API connects to the Redis server and adds a new element to the sorted set 'roadmap'. It uses the 'NX' flag with ZADD to prevent overwriting existing feature requests with the same title. Input is expected in the request body as JSON with a 'title' field. Output is a JSON object indicating success or an error message.

```javascript
import Redis from "ioredis";
import { fixUrl } from "./utils";

module.exports = async (req, res) => {
  let redis = new Redis(fixUrl(process.env.REDIS_URL));
  const body = req.body;
  const title = body["title"];
  if (!title) {
    redis.quit();
    res.json({
      error: "Feature can not be empty",
    });
  } else if (title.length < 70) {
    await redis.zadd("roadmap", "NX", 1, title);
    redis.quit();
    res.json({
      body: "success",
    });
  } else {
    redis.quit();
    res.json({
      error: "Max 70 characters please.",
    });
  }
};

```

--------------------------------

### TypeScript: RatelimitResponse Type Definition

Source: https://upstash.com/docs/redis/sdks/ratelimit-ts/methods

Defines the `RatelimitResponse` type, which includes properties like `success`, `limit`, `remaining`, `reset`, `pending`, `reason`, and `deniedValue`. The `pending` property is crucial for asynchronous operations in serverless environments.

```ts
export type RatelimitResponse = {
  /**
   * Whether the request may pass(true) or exceeded the limit(false)
   */
  success: boolean;
  /**
   * Maximum number of requests allowed within a window.
   */
  limit: number;
  /**
   * How many requests the user has left within the current window.
   */
  remaining: number;
  /**
   * Unix timestamp in milliseconds when the limits are reset.
   */
  reset: number;

  /**
   * For the MultiRegion setup we do some synchronizing in the background, after returning the current limit.
   * Or when analytics is enabled, we send the analytics asynchronously after returning the limit.
   * In most case you can simply ignore this.
   *
   * On Vercel Edge or Cloudflare workers, you need to explicitly handle the pending Promise like this:
   * 
   * ```ts
   * const { pending } = await ratelimit.limit("id")
   * context.waitUntil(pending)
   * ```
   * 
   * See `waitUntil` documentation in
   * [Cloudflare](https://developers.cloudflare.com/workers/runtime-apis/handlers/fetch/#contextwaituntil)
   * and [Vercel](https://vercel.com/docs/functions/edge-middleware/middleware-api#waituntil)
   * for more details.
   * ```
   */
  pending: Promise<unknown>;

  /**
   * Reason behind the result in `success` field.
   * - Is set to "timeout" when request times out
   * - Is set to "cacheBlock" when an identifier is blocked through cache without calling redis because it was
   *    rate limited previously.
   * - Is set to "denyList" when identifier or one of ip/user-agent/country parameters is in deny list. To enable
   *    deny list, see `enableProtection` parameter. To edit the deny list, see the Upstash Ratelimit Dashboard
   *    at https://console.upstash.com/ratelimit.
   * - Is set to undefined if rate limit check had to use Redis. This happens in cases when `success` field in
   *    the response is true. It can also happen the first time sucecss is false.
   */
  reason?: RatelimitResponseType;

  /**
   * The value which was in the deny list if reason: "denyList"
   */
  deniedValue?: string;
};
```

--------------------------------

### BITOP Redis Command

Source: https://upstash.com/docs/redis/sdks/ts/commands/bitmap/bitop

Perform bitwise operations (AND, OR, XOR, NOT) between strings stored in Redis keys and save the result to a destination key.

```APIDOC
## BITOP Redis Command

### Description
Performs bitwise operations between strings. The `BITOP` command in Redis is used to perform bitwise operations on multiple keys (or Redis strings) and store the result in a destination key. It is primarily used for performing logical AND, OR, XOR, and NOT operations on binary data stored in Redis.

### Method
`BITOP`

### Endpoint
`/websites/upstash-redis` (This represents a conceptual endpoint for the Redis command, not a RESTful API)

### Parameters
#### Path Parameters
None

#### Query Parameters
None

#### Request Body
- **operation** (string) - Required - Specifies the type of bitwise operation to perform, which can be one of the following: `AND`, `OR`, `XOR`, or `NOT`.
- **destinationKey** (string) - Required - The key to store the result of the operation in.
- **sourceKeys** (array of strings) - Required - One or more keys to perform the operation on.

### Request Example
```ts
await redis.bitop("AND", "destKey", "sourceKey1", "sourceKey2");
```

### Response
#### Success Response (200)
- **Result** (integer) - The size of the string stored in the destination key.

#### Response Example
```json
10
```
```

--------------------------------

### MGET Command

Source: https://upstash.com/docs/redis/sdks/py/commands/string/mget

Loads multiple keys from Redis in a single operation. This operation is billed as a single command.

```APIDOC
## MGET

### Description
Loads multiple keys from Redis in one go. For billing purposes, this counts as a single command.

### Method
GET

### Endpoint
/websites/upstash-redis

### Parameters
#### Query Parameters
- **keys** (List[str]) - Required - Multiple keys to load from Redis.

### Request Example
```py
redis.set("key1", "value1")
redis.set("key2", "value2")
redis.mget("key1", "key2")
```

### Response
#### Success Response (200)
- **values** (List[str]) - An array of values corresponding to the keys passed in. If a key doesn't exist, the value will be `None`.

#### Response Example
```json
["value1", "value2"]
```
```

--------------------------------

### Calculate Set Difference with TypeScript (Upstash Redis)

Source: https://upstash.com/docs/redis/sdks/ts/commands/set/sdiff

Demonstrates how to use the SDIFF command with Upstash Redis in TypeScript. It first adds elements to two sets, 'set1' and 'set2', and then calculates the difference, printing the result. The command takes the keys of the sets as arguments.

```typescript
await redis.sadd("set1", "a", "b", "c"); 
await redis.sadd("set2", "c", "d", "e"); 
const diff =  await redis.sdiff("set1", "set2");
console.log(diff); // ["a", "b"]
```

--------------------------------

### JSON.OBJLEN

Source: https://upstash.com/docs/redis/sdks/py/commands/json/objlen

Reports the number of keys in the JSON object at a specified path within a Redis key.

```APIDOC
## JSON.OBJLEN

### Description
Reports the number of keys in the JSON object at `path` in `key`.

### Method
N/A (This is a Redis command, not a REST API endpoint)

### Endpoint
N/A

### Parameters
#### Path Parameters
None

#### Query Parameters
None

#### Request Body
None

### Request Example
```py
lengths = redis.json.objlen("key", "$.path")
```

### Response
#### Success Response (200)
- **(List[int])** - The number of keys in the objects.

#### Response Example
```json
[
  1
]
```
```

--------------------------------

### MSETNX - Upstash Redis

Source: https://upstash.com/docs/redis/sdks/ts/commands/string/msetnx

The MSETNX command atomically sets multiple key-value pairs in Redis. It will only set the keys if none of them already exist. This operation is billed as a single command.

```APIDOC
## MSETNX

### Description
Sets multiple keys in one go unless they exist already. For billing purposes, this counts as a single command.

### Method
POST

### Endpoint
/websites/upstash-redis

### Parameters
#### Request Body
- **keys** (Record<string, TValue>) - Required - An object where the keys are the keys to set, and the values are the values to set.

### Request Example
```json
{
  "command": "MSETNX",
  "args": [
    {
      "key1": "value1",
      "key2": "value2"
    }
  ]
}
```

### Response
#### Success Response (200)
- **result** (boolean) - `True` if all keys were set, `False` if at least one key was not set.

#### Response Example
```json
{
  "result": true
}
```
```

--------------------------------

### Retrieve Same Path from Multiple JSON Docs (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/json/mget

This snippet demonstrates how to use the JSON.MGET command in TypeScript to fetch values from a common path within multiple JSON documents stored in Redis. It requires the redis client library and takes an array of keys and a JSON path string as input, returning an array of values found at that path.

```typescript
const values = await redis.json.mget(["key1", "key2"],  "$.path.to.somewhere");
```

--------------------------------

### JSON.ARRLEN

Source: https://upstash.com/docs/redis/sdks/ts/commands/json/arrlen

Report the length of the JSON array at `path` in `key`.

```APIDOC
## JSON.ARRLEN

### Description
Report the length of the JSON array at `path` in `key`.

### Method
(Not applicable - this is a Redis command)

### Endpoint
(Not applicable - this is a Redis command)

### Parameters
#### Path Parameters
(Not applicable)

#### Query Parameters
(Not applicable)

#### Request Body
- **key** (string) - Required - The key of the json entry.
- **path** (string) - Optional - The path of the array. Defaults to `$`.

### Request Example
```ts
const length = await redis.json.arrlen("key", "$.path.to.array");
```

### Response
#### Success Response (200)
- **integer[]** - Required - The length of the array.

#### Response Example
```json
10
```
```

--------------------------------

### JSON.ARRINSERT

Source: https://upstash.com/docs/redis/sdks/ts/commands/json/arrinsert

Inserts JSON values into an array at a specified path and index. Elements at and after the index are shifted to the right.

```APIDOC
## JSON.ARRINSERT

### Description
Inserts the JSON values into the array at the specified path before the given index. This operation shifts existing elements to the right.

### Method
`JSON.ARRINSERT`

### Endpoint
`/websites/upstash-redis

### Parameters
#### Path Parameters
None

#### Query Parameters
None

#### Request Body
- **key** (string) - Required - The key of the JSON entry.
- **path** (string) - Optional (default: "$") - The path to the array within the JSON document.
- **index** (integer) - Required - The index at which to insert the new values. Insertion happens *before* this index.
- **values** (...TValue[]) - Required - One or more values to insert into the array.

### Request Example
```ts
const length = await redis.json.arrinsert("key", "$.path.to.array", 2, "a", "b");
```

### Response
#### Success Response (200)
- **Response** (integer[]) - Required - An array containing the new lengths of the affected arrays after the insertion.

#### Response Example
```json
[3] 
```
```

--------------------------------

### LINSERT Command

Source: https://upstash.com/docs/redis/sdks/py/commands/list/linsert

Inserts an element into a list before or after a specified pivot element.

```APIDOC
## LINSERT

### Description
Inserts an element into a list before or after a specified pivot element.

### Method
POST

### Endpoint
/websites/upstash-redis

### Parameters
#### Request Body
- **key** (str) - Required - The key of the list.
- **direction** (string: "BEFORE" | "AFTER") - Required - Whether to insert the element before or after pivot.
- **pivot** (Any) - Required - The element to insert before or after.
- **value** (Any) - Required - The element to insert.

### Request Example
```json
{
  "key": "my-list",
  "direction": "BEFORE",
  "pivot": "element-to-find",
  "value": "new-element"
}
```

### Response
#### Success Response (200)
- **return_value** (int) - The list length after insertion, `0` when the list doesn't exist or `-1` when pivot was not found.

#### Response Example
```json
{
  "return_value": 4
}
```
```

--------------------------------

### Configure Upstash Redis for Laravel Queues

Source: https://upstash.com/docs/redis/quickstarts/laravel

Configures Laravel's queue system to use Upstash Redis as the connection driver by setting QUEUE_CONNECTION to 'redis' in the .env file. This allows for efficient background job processing using Redis.

```.env
QUEUE_CONNECTION="redis"
```

--------------------------------

### LPOP Command

Source: https://upstash.com/docs/redis/sdks/ts/commands/list/lpop

Removes and returns the first element(s) of a list. Supports popping a single element or multiple elements.

```APIDOC
## LPOP

### Description
Remove and return the first element(s) of a list.

### Method
POST

### Endpoint
/websites/upstash-redis

### Parameters
#### Request Body
- **key** (string) - Required - The key of the list.
- **count** (integer) - Optional - How many elements to pop. If not specified, a single element is popped.

### Request Example
```json
{
  "key": "myList",
  "count": 2
}
```

### Response
#### Success Response (200)
- **response** (TValue | TValue[] | null) - The popped element(s). If `count` was specified, an array of elements is returned, otherwise a single element is returned. If the list is empty, `null` is returned.

#### Response Example
```json
{
  "response": ["element1", "element2"]
}
```

```json
{
  "response": "element1"
}
```

```json
{
  "response": null
}
```
```

--------------------------------

### Configure Upstash Redis for Laravel Caching

Source: https://upstash.com/docs/redis/quickstarts/laravel

Configures Laravel to use Upstash Redis as the caching driver by updating the CACHE_STORE to 'redis' and specifying the Redis cache database in the .env file. This enhances application performance through Redis-based caching.

```.env
CACHE_STORE="redis"
REDIS_CACHE_DB="0"
```

--------------------------------

### Vercel Edge Middleware with Global Rate Limiting and Auth

Source: https://context7.com/context7/upstash-redis/llms.txt

This snippet illustrates how to implement global rate limiting and authentication at the edge using Vercel Edge Middleware with Upstash Redis. It utilizes the Cloudflare-compatible Redis import for efficient edge operations and sets response headers for rate limit status. Authentication is handled by checking a Bearer token in the request headers.

```typescript
// middleware.ts
import { Redis } from "@upstash/redis/cloudflare";
import { Ratelimit } from "@upstash/ratelimit";
import { NextRequest, NextResponse } from "next/server";

const redis = new Redis({
  url: process.env.UPSTASH_REDIS_REST_URL!,
  token: process.env.UPSTASH_REDIS_REST_TOKEN!,
});

const ratelimit = new Ratelimit({
  redis,
  limiter: Ratelimit.slidingWindow(20, "10 s"),
  analytics: true,
});

export async function middleware(request: NextRequest) {
  const ip = request.ip || "anonymous";
  const { success, pending, limit, remaining, reset } = await ratelimit.limit(ip);

  const response = success
    ? NextResponse.next()
    : NextResponse.json({ error: "Too Many Requests" }, { status: 429 });

  // Add rate limit headers
  response.headers.set("X-RateLimit-Limit", limit.toString());
  response.headers.set("X-RateLimit-Remaining", remaining.toString());
  response.headers.set("X-RateLimit-Reset", new Date(reset).toISOString());

  // Check authentication
  const token = request.headers.get("authorization")?.replace("Bearer ", "");
  if (token) {
    const session = await redis.get(`session:${token}`);
    if (session) {
      response.headers.set("X-User-Id", JSON.parse(session).userId);
    }
  }

  // Wait for background operations
  request.waitUntil(pending);

  return response;
}

export const config = {
  matcher: "/api/:path*",
};

```

--------------------------------

### Pass Environment Variables to SST Application

Source: https://upstash.com/docs/redis/quickstarts/ion

Configures the SST application to pass the Upstash Redis environment variables to the deployed Next.js application. This ensures the Redis client can access the connection details at runtime.

```typescript
/// <reference path="./.sst/platform/config.d.ts" />

export default $config({
  app(input) {
    return {
      name: "my-app",
      removal: input?.stage === "production" ? "retain" : "remove",
      home: "aws",
    };
  },
  async run() {
    new sst.aws.Nextjs("MyWeb", {
      environment: {
        UPSTASH_REDIS_REST_URL: process.env.UPSTASH_REDIS_REST_URL || "",
        UPSTASH_REDIS_REST_TOKEN: process.env.UPSTASH_REDIS_REST_TOKEN || "",
      },
    });
  },
});
```

--------------------------------

### Create Todos Table Migration

Source: https://upstash.com/docs/redis/tutorials/laravel_caching

Defines the database schema for the 'todos' table, including an auto-incrementing ID, a string 'title' column, and standard timestamps. This migration file is used to create the table structure in your database.

```php
<?php

use IlluminateDatabaseMigrationsMigration;
use IlluminateDatabaseSchemaBlueprint;
use IlluminateSupportFacadesSchema;

return new class extends Migration
{
    /**
     * Run the migrations.
     */
    public function up(): void
    {
        Schema::create('todos', function (Blueprint $table) {
            $table->id();
            $table->string('title');
            $table->timestamps();
        });
    }

    /**
     * Reverse the migrations.
     */
    public function down(): void
    {
        Schema::dropIfExists('todos');
    }
};

```

--------------------------------

### Set List Element by Index in Python

Source: https://upstash.com/docs/redis/sdks/py/commands/list/lset

Demonstrates how to use the LSET command with the Upstash Redis Python SDK. It shows setting an element at a valid index and attempting to set it at an invalid index, verifying the results with LRANGE.

```python
redis.rpush("mylist", "one", "two", "three")

assert redis.lset("mylist", 1, "Hello") == True

assert redis.lrange("mylist", 0, -1) == ["one", "Hello", "three"]

assert redis.lset("mylist", 5, "Hello") == False

assert redis.lrange("mylist", 0, -1) == ["one", "Hello", "three"]
```

--------------------------------

### Bind Redis Secrets to SST Stack

Source: https://upstash.com/docs/redis/quickstarts/sst-v2

This TypeScript code defines the `Default` stack for your SST application. It declares the Redis URL and token as secrets using `Config.Secret` and binds them to the `NextjsSite` construct. This makes the secrets available to your Next.js application at runtime.

```typescript
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

--------------------------------

### LPOP Command

Source: https://upstash.com/docs/redis/sdks/py/commands/list/lpop

Removes and returns the first element(s) from a list stored at the specified key.

```APIDOC
## LPOP

### Description
Removes and returns the first element(s) of a list.

### Method
POST

### Endpoint
/websites/upstash-redis

### Parameters
#### Request Body
- **key** (str) - Required - The key of the list.
- **count** (int) - Optional - How many elements to pop. If not specified, a single element is popped.

### Request Example
```py
# Single element pop
redis.lpop("mylist")

# Multiple elements pop
redis.lpop("mylist", 2)
```

### Response
#### Success Response (200)
- **Response** (str | List[str] | None) - The popped element(s). If `count` was specified, an array of elements is returned, otherwise a single element is returned. If the list is empty, `None` is returned.

#### Response Example
```json
"one"
```

```json
["one", "two"]
```

```json
null
```
```

--------------------------------

### Trigger IP Deny List Update and Check Status in TypeScript

Source: https://upstash.com/docs/redis/sdks/ratelimit-ts/traffic-protection

This snippet shows how to use the `limit` method to apply rate limiting and trigger an IP deny list update if necessary. It returns `success` for the rate limit decision and `pending` for the asynchronous update status. Awaiting `pending` ensures the update completes before proceeding.

```typescript
const { success, pending } = await ratelimit.limit(
  content,
  {ip: "ip-address"}
);

await pending;
```

--------------------------------

### LINDEX

Source: https://upstash.com/docs/redis/sdks/ts/commands/list/lindex

Retrieves the element at a specific index from a list stored at a given key. Supports zero-based and negative indexing.

```APIDOC
## LINDEX

### Description
Returns the element at index `index` in the list stored at `key`. The index is zero-based. Negative indices can be used to designate elements starting at the tail of the list.

### Method
GET (or POST depending on Redis client implementation)

### Endpoint
`/lindex` (Conceptual endpoint, actual usage depends on Redis client)

### Parameters
#### Query Parameters (or part of request body for POST)
- **key** (string) - Required - The key of the list.
- **index** (number) - Required - The zero-based index of the element to return.

### Request Example
```ts
await redis.lpush("myList", "item1", "item2", "item3");
const element = await redis.lindex("myList", 1);
console.log(element); // "item2"
```

### Response
#### Success Response (200)
- **TValue | null** - The value of the element at the specified index. Returns `null` if the index is out of range.
```

--------------------------------

### SUNIONSTORE

Source: https://upstash.com/docs/redis/sdks/py/commands/set/sunionstore

Performs a set union operation on multiple source sets and stores the result in a destination set.

```APIDOC
## SUNIONSTORE

### Description
Returns the union between sets and stores the resulting set in a key.

### Method
POST

### Endpoint
/websites/upstash-redis

### Parameters
#### Request Body
- **destination** (str) - Required - The key of the set to store the resulting set in.
- **keys** (*List[str]) - Required - The keys of the sets to perform the union operation on.

### Request Example
```json
{
  "command": "SUNIONSTORE",
  "args": ["destination", "set1", "set2"]
}
```

### Response
#### Success Response (200)
- **result** (set[str]) - The members of the resulting set.

#### Response Example
```json
{
  "result": ["a", "b", "c", "d", "e"]
}
```
```

--------------------------------

### TypeScript Supabase Function for Redis Counter

Source: https://upstash.com/docs/redis/quickstarts/supabase

This TypeScript code defines a Supabase edge function that uses Upstash Redis to count function invocations. It connects to Redis using environment variables for the URL and token, then increments a hash counter based on the Deno region or 'localhost'. It retrieves and formats all counter data before returning it. Dependencies include 'deno.land/std/http/server.ts' and 'deno.land/x/upstash_redis/mod.ts'.

```typescript
import { serve } from "https://deno.land/std@0.177.0/http/server.ts";
import { Redis } from "https://deno.land/x/upstash_redis@v1.19.3/mod.ts";
console.log(`Function "upstash-redis-counter" up and running!`);
serve(async (_req) => {
  try {
    const redis = new Redis({
      url: Deno.env.get("UPSTASH_REDIS_REST_URL")!,
      token: Deno.env.get("UPSTASH_REDIS_REST_TOKEN")!,
    });
    const deno_region = Deno.env.get("DENO_REGION");
    if (deno_region) {
      // Increment region counter
      await redis.hincrby("supa-edge-counter", deno_region, 1);
    } else {
      // Increment localhost counter
      await redis.hincrby("supa-edge-counter", "localhost", 1);
    }
    // Get all values
    const counterHash: Record<string, number> | null = await redis.hgetall(
      "supa-edge-counter"
    );
    const counters = Object.entries(counterHash!)
      .sort(([, a], [, b]) => b - a) // sort desc
      .reduce(
        (r, [k, v]) => ({
          total: r.total + v,
          regions: { ...r.regions, [k]: v },
        }),
        {
          total: 0,
          regions: {},
        }
      );
    return new Response(JSON.stringify({ counters }), { status: 200 });
  } catch (error) {
    return new Response(JSON.stringify({ error: error.message }), {
      status: 200,
    });
  }
});

```

--------------------------------

### Insert JSON Array Elements (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/json/arrinsert

Demonstrates how to use the JSON.ARRINSERT command in TypeScript to insert elements into a JSON array. This command requires the key, path to the array, the index for insertion, and the values to be inserted. It returns the updated array length.

```typescript
const length = await redis.json.arrinsert("key", "$.path.to.array", 2, "a", "b");
```

--------------------------------

### Evaluate Cached Lua Script with EVALSHA (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/scripts/evalsha

Executes a Lua script on the Redis server using its SHA1 hash. This method is efficient for repeated script executions as it avoids sending the script content over the network each time. It requires the script's SHA1 hash, a list of keys accessed by the script, and any arguments passed to the script.

```python
result = redis.evalsha("fb67a0c03b48ddbf8b4c9b011e779563bdbc28cb", args=["hello"])
assert result == "hello"
```

--------------------------------

### Push Elements to List End (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/list/rpush

Demonstrates how to use the RPUSH command in TypeScript to add elements to the end of a Redis list. The command takes the key and one or more elements as arguments and returns the list's new length. Ensure the 'redis' client is properly initialized.

```typescript
const length1 = await redis.rpush("key", "a", "b", "c"); 
console.log(length1); // 3
const length2 = await redis.rpush("key", "d"); 
console.log(length2); // 4
```

--------------------------------

### Execute Redis Pipeline in TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/transaction

Executes multiple Redis commands in a pipeline for batched execution. Commands are sent at once but may be interleaved with other client commands. Uses the `pipeline` method to create a pipeline object and `exec` to run it.

```ts
const p = redis.pipeline();
p.set("foo", "bar");
p.get("foo");
const res = await p.exec();
```

--------------------------------

### Customizing Request Rates with Upstash Redis

Source: https://upstash.com/docs/redis/sdks/ratelimit-py/features

Illustrates how to specify a custom rate (token cost) for individual requests when using Upstash Redis rate limiting. This feature is valuable for scenarios where different operations have varying consumption rates, such as batch processing or token-based billing. It requires the `upstash_ratelimit` and `upstash_redis` libraries.

```python
from upstash_ratelimit import Ratelimit, FixedWindow
from upstash_redis import Redis

ratelimit = Ratelimit(
    redis=Redis.from_env(),
    limiter=FixedWindow(max_requests=10, window=10),
)

# pass rate as 5 to subtract 5 from the number of
# allowed requests in the window:
identifier = "api"
response = ratelimit.limit(identifier, rate=5)
```

--------------------------------

### Evaluate Cached Lua Script with EVALSHA (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/scripts/evalsha

This code snippet demonstrates how to use the EVALSHA command in Upstash Redis with TypeScript. It requires the redis client instance, the SHA1 hash of the cached Lua script, an array of keys, and an array of arguments. The function returns the result of the script execution.

```typescript
const result = await redis.evalsha("fb67a0c03b48ddbf8b4c9b011e779563bdbc28cb", [], ["hello"]);
console.log(result) // "hello"
```

--------------------------------

### HSETNX

Source: https://upstash.com/docs/redis/sdks/py/commands/hash/hsetnx

Writes a field to a hash but only if the field does not exist.

```APIDOC
## HSETNX

### Description
Write a field to a hash but only if the field does not exist.

### Method
POST

### Endpoint
/websites/upstash-redis

### Parameters
#### Request Body
- **key** (str) - Required - The key of the hash.
- **field** (str) - Required - The name of the field.
- **value** (Any) - Required - The value to set.

### Request Example
```json
{
  "key": "myhash",
  "field": "field1",
  "value": "Hello"
}
```

### Response
#### Success Response (200)
- **result** (bool) - `True` if the field was set, `False` if it already existed.

#### Response Example
```json
{
  "result": true
}
```
```

--------------------------------

### Perform Set Union and Store Result (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/set/sunionstore

This Python code snippet demonstrates how to use the SUNIONSTORE command with Upstash Redis. It first adds members to two sets, 'set1' and 'set2', and then performs a union operation, storing the result in a new set named 'destination'.

```python
redis.sadd("set1", "a", "b", "c"); 
redis.sadd("set2", "c", "d", "e"); 
redis.sunionstore("destination", "set1", "set2")
```

--------------------------------

### HMGET Command

Source: https://upstash.com/docs/redis/sdks/py/commands/hash/hmget

Retrieves multiple fields and their values from a hash stored at a specified key in Upstash Redis.

```APIDOC
## HMGET

### Description
Return the requested fields and their values from a hash.

### Method
GET (Implicit, typically used with a client library)

### Endpoint
`/` (Command executed via client)

### Parameters
#### Path Parameters
None

#### Query Parameters
None

#### Request Body
**key** (str) - Required - The key of the hash.
**fields** (*List[str]) - Required - One or more fields to get.

### Request Example
```py
# Assuming 'redis' is an initialized Upstash Redis client
redis.hset("myhash", values={"field1": "Hello", "field2": "World"})
result = redis.hmget("myhash", "field1", "field2")
print(result) # Output: ['Hello', 'World']
```

### Response
#### Success Response (200)
**List[str | None]** - An object containing the fields and their values. If a field does not exist, its value will be null.
```

--------------------------------

### Execute Read-Only Lua Script with EVAL_RO in TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/scripts/eval_ro

This snippet demonstrates how to execute a read-only Lua script using the EVAL_RO command in TypeScript with Upstash Redis. It requires the Redis client instance, the Lua script string, an array of keys, and an array of arguments. The output is the result returned by the Lua script.

```typescript
const script = "\n      return ARGV[1]\n  "
  const result = await redis.evalRo(script, [], ["hello"]);
  console.log(result) // "hello"
```

--------------------------------

### Command Pipelining with Curl

Source: https://upstash.com/docs/redis/features/restapi

Illustrates how to send multiple Redis commands in a single HTTP request to the Upstash Redis REST API using the pipeline endpoint. This enhances throughput by reducing round-trip times. The commands are provided as a JSON array in the request body.

```shell
curl -X POST https://us1-merry-cat-32748.upstash.io/pipeline \
 -H "Authorization: Bearer $TOKEN" \
 -d '
    [
      ["CMD_A", "arg0", "arg1", ..., "argN"],
      ["CMD_B", "arg0", "arg1", ..., "argM"],
      ...
    ]
    '

# Response syntax:
# [{"result":"RESPONSE_A"},{"result":"RESPONSE_B"},{"error":"ERR ..."}, ...]

curl -X POST https://us1-merry-cat-32748.upstash.io/pipeline \
 -H "Authorization: Bearer 2553feg6a2d9842h2a0gcdb5f8efe9934" \
 -d '
    [
      ["SET", "key1", "valuex"],
      ["SETEX", "key2", 13, "valuez"],
      ["INCR", "key1"],
      ["ZADD", "myset", 11, "item1", 22, "item2"]
    ]
    '

# Pipeline response example:
# [
#   { "result": "OK" },
#   { "result": "OK" },
#   { "error": "ERR value is not an int or out of range" },
#   { "result": 2 }
# ]
```

--------------------------------

### Configure Upstash Redis Credentials in .env

Source: https://upstash.com/docs/redis/quickstarts/laravel

Sets Upstash Redis connection details in the Laravel environment file (.env). This includes the Redis host endpoint, port, and password, enabling Laravel to connect to the Upstash Redis database.

```.env
REDIS_HOST="<YOUR_ENDPOINT>"
REDIS_PORT=6379
REDIS_PASSWORD="<YOUR_PASSWORD>"
```

--------------------------------

### Write Fields to Redis Hash using HSET (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/hash/hset

This snippet demonstrates how to use the HSET command to add multiple field-value pairs to a Redis hash. It requires the Upstash Redis client and takes the hash key and a fields object as input. The function returns the count of fields added.

```typescript
await redis.hset("key", {
  id: 1,
  username: "chronark",
  name: "andreas"
  });
```

--------------------------------

### Set Key with String Value - TypeScript

Source: https://upstash.com/docs/redis/sdks/ts/commands/string/set

Sets a key to hold a string value. If the provided value is not a string, it will be JSON.stringified. This is the basic usage of the SET command.

```typescript
await redis.set("my-key", {my: "value"});
```

--------------------------------

### JSON.GET Command

Source: https://upstash.com/docs/redis/sdks/ts/commands/json/get

Retrieves a single value from a JSON document based on the provided key and path.

```APIDOC
## JSON.GET

### Description
Get a single value from a JSON document.

### Method
GET (or equivalent for command-based APIs)

### Endpoint
Not applicable for command-based APIs like Upstash Redis.

### Parameters
#### Path Parameters
None

#### Query Parameters
None

#### Request Body
This command operates on keys and arguments, not a traditional request body.

- **key** (string) - Required - The key of the JSON entry.
- **options** (object) - Optional - Configuration for retrieval.
  - **indent** (string) - Optional - Sets the indentation string for nested levels.
  - **newline** (string) - Optional - Sets the string that's printed at the end of each line.
  - **space** (string) - Optional - Sets the string that is put between a key and a value.
- **paths** (...string[]) - Required, defaults to $" - One or more paths to retrieve from the JSON document.

### Request Example
```ts
// Basic usage
const value = await redis.json.get("key", "$.path.to.somewhere");

// With options
const valueWithOptions = await redis.json.get("key", {
    indent: "  ",
    newline: "\n",
    space: " ",
}, "$.path.to.somewhere");
```

### Response
#### Success Response (200 OK)
- **(TValue | null)[]** (array) - The value at the specified path or `null` if the path does not exist.
```

--------------------------------

### GETSET

Source: https://upstash.com/docs/redis/sdks/py/commands/string/getset

Retrieves the value of a specified key and replaces it with a new value atomically.

```APIDOC
## GETSET

### Description
Retrieves the value of the specified key and replaces it with a new value atomically.

### Method
POST

### Endpoint
/websites/upstash-redis

### Parameters
#### Path Parameters
None

#### Query Parameters
None

#### Request Body
- **key** (str) - Required - The key to get and set.
- **value** (Any) - Required - The new value to store.

### Request Example
```json
{
  "key": "mykey",
  "value": "newvalue"
}
```

### Response
#### Success Response (200)
- **response** (Any) - The previous value stored at the key, or `None` if the key did not exist.

#### Response Example
```json
{
  "response": "oldvalue"
}
```
```

--------------------------------

### SET Command

Source: https://upstash.com/docs/redis/sdks/ts/commands/string/set

Sets a key to hold a string value. Supports various options for expiration and conditional setting.

```APIDOC
## SET /SET

### Description
Sets a key to hold a string value. If the key already holds a value, it will be overwritten unless the NX or XX option is used.

### Method
POST

### Endpoint
/SET

### Parameters
#### Request Body
- **key** (string) - Required - The key to set.
- **value** (TValue) - Required - The value to store. If not a string, it will be JSON.stringified.
- **opts** (object) - Optional - Options for the SET command.
  - **get** (boolean) - Optional - If true, returns the old value of the key instead of 'OK'.
  - **ex** (integer) - Optional - Sets an expiration time in seconds.
  - **px** (integer) - Optional - Sets an expiration time in milliseconds.
  - **exat** (integer) - Optional - Sets an expiration timestamp in seconds.
  - **pxat** (integer) - Optional - Sets an expiration timestamp in milliseconds.
  - **keepTtl** (boolean) - Optional - If true, preserves the existing TTL when updating a key.
  - **nx** (boolean) - Optional - If true, only sets the key if it does not already exist.
  - **xx** (boolean) - Optional - If true, only sets the key if it already exists.

### Request Example
```json
{
  "key": "my-key",
  "value": {"my": "value"},
  "opts": {
    "ex": 60,
    "xx": true
  }
}
```

### Response
#### Success Response (200)
- **result** (string) - Returns 'OK' on success, or the old value if 'get' option is used.

#### Response Example
```json
{
  "result": "OK"
}
```
```

--------------------------------

### HGETALL - Retrieve all fields from a hash

Source: https://upstash.com/docs/redis/sdks/ts/commands/hash/hgetall

The HGETALL command retrieves all fields and values from a hash stored at the specified key.

```APIDOC
## HGETALL

### Description
Retrieves all fields and values from a hash stored at the specified key.

### Method
GET (Conceptual - this is a Redis command, not a direct HTTP endpoint)

### Endpoint
(Not applicable for Redis commands)

### Parameters
#### Path Parameters
(Not applicable for Redis commands)

#### Query Parameters
(Not applicable for Redis commands)

#### Request Body
- **key** (string) - Required - The key of the hash to retrieve.

### Request Example
```typescript
await redis.hgetall("key");
```

### Response
#### Success Response
- **TValue | null** - An object containing all fields and values in the hash, or null if the key does not exist.

#### Response Example
```json
{
  "field1": "value1",
  "field2": "value2"
}
```
```

--------------------------------

### POST /publish/{channel}/{message} (Publish Command)

Source: https://upstash.com/docs/redis/features/restapi

Publish a message to a specified Redis channel.

```APIDOC
## POST /publish/{channel}/{message}

### Description
Publish a message to a specified Redis channel.

### Method
POST

### Endpoint
/publish/{channel}/{message}

### Parameters
#### Path Parameters
- **channel** (string) - Required - The name of the channel to publish to.
- **message** (string) - Required - The message content to publish.

#### Headers
- **Authorization**: `Bearer <TOKEN>` - Required

### Response
#### Success Response (200)
- **result** (integer) - The number of clients that received the message.

### Response Example
```json
{
  "result": 1
}
```
```

--------------------------------

### Set JSON Value using Python Redis Client

Source: https://upstash.com/docs/redis/sdks/py/commands/json/set

Demonstrates how to set a JSON value at a specified path within a Redis key using the Python Redis client. This function requires the key, path, and value as arguments. Optional nx and xx arguments can be used to conditionally set the value.

```python
redis.json.set(key, "$.path", value)
```

```python
value = ...
redis.json.set(key, "$.path", value, nx=true)
```

```python
value = ...
redis.json.set(key, "$.path", value, xx=true)
```

--------------------------------

### Increment Key Value with Upstash Redis (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/string/incrby

Demonstrates how to use the INCRBY command in Upstash Redis to increment an integer value associated with a key. This function requires the 'redis' client to be initialized and expects the key and the increment amount as arguments.

```typescript
await redis.set("key", 6);
await redis.incrby("key", 4);
// returns 10
```

--------------------------------

### RESP2 Format Responses

Source: https://upstash.com/docs/redis/features/restapi

This section describes how to obtain responses in the RESP2 binary format by setting the 'Upstash-Response-Format' header to 'resp2'. This is useful for clients that expect the standard Redis protocol response.

```APIDOC
## RESP2 Format Responses

REST API returns a JSON response by default and the response content type is set to `application/json`.

If you prefer the binary response in RESP2 format, you can achieve this by setting the `Upstash-Response-Format` header to `resp2`. In this case, the response content type is set to `application/octet-stream` and the raw response is returned as binary similar to a TCP-based Redis client.

The default value for this option is `json`. Any format other than `json` and `resp2` is not allowed and will result in a HTTP 400 Bad Request.

This option is not applicable to `/multi-exec` transactions endpoint, as it only returns response in JSON format. Additionally, setting the `Upstash-Encoding` header to `base64` is not permitted when the `Upstash-Response-Format` is set to `resp2` and will result in a HTTP 400 Bad Request.

### Request Example (SET with RESP2 Format)

```shell
curl https://us1-merry-cat-32748.upstash.io/SET/foo/bar \
 -H "Authorization: Bearer 2553feg6a2d9842h2a0gcdb5f8efe9934" \
 -H "Upstash-Reponse-Format: resp2"
```

### Response Example (SET with RESP2 Format)

```
+OK\r\n
```

### Request Example (GET with RESP2 Format)

```shell
curl https://us1-merry-cat-32748.upstash.io/GET/foo \
 -H "Authorization: Bearer 2553feg6a2d9842h2a0gcdb5f8efe9934" \
 -H "Upstash-Reponse-Format: resp2"
```

### Response Example (GET with RESP2 Format)

```
$3\r\nbar\r\n
```
```

--------------------------------

### Evaluate Cached Read-Only Lua Script (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/scripts/evalsha_ro

Executes a read-only Lua script on the server using its SHA1 hash. This requires the SHA1 hash of the script, a list of keys accessed by the script, and a list of arguments for the script. The response is the result of the script execution.

```python
result = redis.evalsha_ro("fb67a0c03b48ddbf8b4c9b011e779563bdbc28cb", args=["hello"])
assert result == "hello"
```

--------------------------------

### Check Set Membership with SISMEMBER (Python)

Source: https://upstash.com/docs/redis/sdks/py/commands/set/sismember

This Python snippet demonstrates how to use the SISMEMBER command to check if a member exists in a Redis set. It first adds members to a set and then verifies the presence of one of the members.

```python
redis.sadd("set", "a", "b", "c")

assert redis.sismember("set", "a") == True
```

--------------------------------

### Set Multiple Bitfield Values in Python

Source: https://upstash.com/docs/redis/sdks/py/commands/bitmap/bitfield

This snippet demonstrates setting multiple values in a Redis bitfield. It initializes an empty key and then sets two 4-bit unsigned integers: one to 16 at offset 0 and another to 1 at offset 4. The command returns the old values for each set operation.

```python
redis.set("mykey", "")

result = redis.bitfield("mykey") \
    .set("u4", 0, 16) \
    .set("u4", 4, 1) \
    .execute()
    
assert result == [0, 1]
```

--------------------------------

### Remove First Element from Redis List (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/list/lpop

Demonstrates how to remove and return the first element from a Redis list using the LPOP command in TypeScript. It first pushes elements to the list and then calls LPOP to retrieve the first one.

```typescript
await redis.rpush("key", "a", "b", "c"); 
const element = await redis.lpop("key");
console.log(element); // "a"
```

--------------------------------

### JSON.OBJKEYS

Source: https://upstash.com/docs/redis/sdks/py/commands/json/objkeys

Retrieves all the keys in the JSON object stored at a specific path within a Redis key.

```APIDOC
## JSON.OBJKEYS

### Description
Return the keys in the object that's referenced by path.

### Method
Not applicable (command-line interface or client library usage).

### Endpoint
Not applicable (command-line interface or client library usage).

### Parameters
#### Path Parameters
None

#### Query Parameters
None

#### Request Body
- **key** (str) - Required - The key of the JSON entry.
- **path** (str) - Optional - The path of the object. Defaults to "$".

### Request Example
```py
redis.json.objkeys("key", "$.path")
```

### Response
#### Success Response (200)
- **keys** (List[List[str]]) - Required - The keys of the object at the specified path.

#### Response Example
```json
[
  ["key1", "key2", "key3"]
]
```
```

--------------------------------

### APPEND

Source: https://upstash.com/docs/redis/sdks/py/commands/string/append

Appends a string value to a previously stored string at the specified key. If the key does not exist, it is created with the appended value.

```APIDOC
## APPEND

### Description
Append a value to a string stored at key.

### Method
POST

### Endpoint
/websites/upstash-redis

### Parameters
#### Request Body
- **key** (str) - Required - The key to append the value to.
- **value** (str) - Required - The value to append.

### Request Example
```json
{
  "key": "mykey",
  "value": "appended_value"
}
```

### Response
#### Success Response (200)
- **response** (int) - Required - How many characters were added to the string.

#### Response Example
```json
11
```
```

--------------------------------

### INCRBY Command

Source: https://upstash.com/docs/redis/sdks/py/commands/string/incrby

Increments the integer value of a key by a given number. Initializes the key to 0 if it doesn't exist.

```APIDOC
## INCRBY

### Description
Increment the integer value of a key by a given number. If a key does not exist, it is initialized as 0 before performing the operation. An error is returned if the key contains a value of the wrong type or contains a string that can not be represented as integer.

### Method
POST

### Endpoint
/websites/upstash-redis

### Parameters
#### Request Body
- **key** (str) - Required - The key to increment.
- **increment** (int) - Required - The amount to increment by.

### Request Example
```json
{
  "key": "mykey",
  "increment": 5
}
```

### Response
#### Success Response (200)
- **value** (int) - The value at the key after the incrementing.

#### Response Example
```json
{
  "value": 10
}
```
```

--------------------------------

### Check Multiple Set Members with SMISMEMBER (TypeScript)

Source: https://upstash.com/docs/redis/sdks/ts/commands/set/smismember

This snippet demonstrates how to use the SMISMEMBER command in TypeScript to verify the presence of multiple elements within a Redis set. It requires an existing Redis client instance. The function takes the set key and an array of members as input and returns an array of 0s and 1s, where 1 signifies existence and 0 signifies non-existence.

```typescript
await redis.sadd("set", "a", "b", "c"); 
const members =  await redis.smismember("set", ["a", "b", "d"]);
console.log(members); // [1, 1, 0]
```

--------------------------------

### RPUSHX Command

Source: https://upstash.com/docs/redis/sdks/py/commands/list/rpushx

The RPUSHX command pushes one or more elements to the end of a list, but only if the list already exists. If the list does not exist, no operation is performed.

```APIDOC
## RPUSHX

### Description
Push an element at the end of the list only if the list exists.

### Method
POST

### Endpoint
/websites/upstash-redis

### Parameters
#### Request Body
- **key** (str) - Required - The key of the list.
- **elements** (*List[str]) - Required - One or more elements to push at the end of the list.

### Request Example
```json
{
  "key": "mylist",
  "elements": ["one", "two", "three"]
}
```

### Response
#### Success Response (200)
- **length** (int) - The length of the list after the push operation. Returns 0 if the list did not exist and thus no element was pushed.

#### Response Example
```json
{
  "length": 3
}
```
```

--------------------------------

### BITPOS Command

Source: https://upstash.com/docs/redis/sdks/py/commands/bitmap/bitpos

Finds the position of the first set or clear bit (bit with a value of 1 or 0) in a Redis string key.

```APIDOC
## BITPOS

### Description
Finds the position of the first set or clear bit (bit with a value of 1 or 0) in a Redis string key.

### Method
`BITPOS` (Redis Command)

### Endpoint
N/A (This is a Redis command, not a REST API endpoint)

### Parameters
#### Path Parameters
None

#### Query Parameters
None

#### Request Body
None

### Request Example
```python
# Example usage with Upstash Redis client
redis.setbit("mykey", 7, 1)
redis.setbit("mykey", 8, 1)

# Find the first set bit (1)
print(redis.bitpos("mykey", 1))  # Output: 7

# Find the first clear bit (0)
print(redis.bitpos("mykey", 0))  # Output: 0

# Find the first set bit within a range (start=0, end=2)
print(redis.bitpos("mykey", 1, 0, 2)) # Output: 0

# Find the first set bit within a range (start=2, end=3)
print(redis.bitpos("mykey", 1, 2, 3)) # Output: -1 (not found)

# Find the first set bit within a specific range
print(redis.bitpos("key", 1, 5, 20)) 
```

### Response
#### Success Response
- **index** (integer) - The index of the first occurrence of the bit in the string. Returns -1 if the bit is not found within the specified range.
```

--------------------------------

### EVALSHA - Evaluate Cached Lua Script

Source: https://upstash.com/docs/redis/sdks/ts/commands/scripts/evalsha

Executes a Lua script on the server using its SHA1 hash. This is more efficient than sending the script content repeatedly, as the script is cached on the server.

```APIDOC
## EVALSHA

### Description
Evaluate a cached Lua script server side. `EVALSHA` is like `EVAL` but instead of sending the script over the wire every time, you reference the script by its SHA1 hash. This is useful for caching scripts on the server side.

### Method
POST

### Endpoint
/websites/upstash-redis

### Parameters
#### Request Body
- **sha** (string) - Required - The sha1 hash of the script.
- **keys** (string[]) - Required - All of the keys accessed in the script.
- **args** (unknown[]) - Required - All of the arguments you passed to the script.

### Request Example
```json
{
  "sha": "fb67a0c03b48ddbf8b4c9b011e779563bdbc28cb",
  "keys": [],
  "args": ["hello"]
}
```

### Response
#### Success Response (200)
- **result** (?) - The result of the script.

#### Response Example
```json
{
  "result": "hello"
}
```
```

--------------------------------

### RESP2 Format Responses with Curl

Source: https://upstash.com/docs/redis/features/restapi

Shows how to obtain responses in the RESP2 binary format from the Upstash Redis REST API using curl. This method is suitable for applications that expect Redis's native RESP2 protocol. It requires setting the 'Upstash-Response-Format' header to 'resp2'.

```shell
curl https://us1-merry-cat-32748.upstash.io/SET/foo/bar \
 -H "Authorization: Bearer 2553feg6a2d9842h2a0gcdb5f8efe9934" \
 -H "Upstash-Reponse-Format: resp2"

# +OK\r\n

curl https://us1-merry-cat-32748.upstash.io/GET/foo \
 -H "Authorization: Bearer 2553feg6a2d9842h2a0gcdb5f8efe9934" \
 -H "Upstash-Reponse-Format: resp2"

# $3\r\nbar\r\n
```

--------------------------------

### POST /subscribe/{channel} (Subscribe Command)

Source: https://upstash.com/docs/redis/features/restapi

Subscribe to a Redis channel using Server-Sent Events (SSE). Incoming messages will be streamed as 'data' lines.

```APIDOC
## POST /subscribe/{channel}

### Description
Subscribe to a Redis channel using Server-Sent Events (SSE). Incoming messages will be streamed as 'data' lines.

### Method
POST

### Endpoint
/subscribe/{channel}

### Parameters
#### Path Parameters
- **channel** (string) - Required - The name of the channel to subscribe to.

#### Headers
- **Accept**: `text/event-stream` - Required
- **Authorization**: `Bearer <TOKEN>` - Required

### Response
#### Success Response (200)
- **data**: (string) - Each line starting with `data:` represents a subscription or message event.

### Response Example
```
data: subscribe,chat,1
data: message,chat,hello
data: message,chat,how are you today?
```
```

--------------------------------

### Upstash Redis REST API - Transactions (Bash)

Source: https://context7.com/context7/upstash-redis/llms.txt

Execute atomic transactions using the multi-exec endpoint for guaranteed all-or-nothing execution of Redis commands. This ensures data consistency even with concurrent operations.

```bash
# Atomic transaction (all or nothing)
curl -X POST https://us1-merry-cat-32748.upstash.io/multi-exec \
  -H "Authorization: Bearer 2553feg6a2d9842h2a0gcdb5f8efe9934" \
  -d '[
    ["SET", "balance:alice", "1000"],
    ["DECRBY", "balance:alice", "100"],
    ["INCRBY", "balance:bob", "100"],
    ["GET", "balance:alice"],
    ["GET", "balance:bob"]
  ]'

# Response: [
#   {"result":"OK"},
#   {"result":900},
#   {"result":100},
#   {"result":"900"},
#   {"result":"100"}
# ]

# All commands execute atomically
# No other commands interleave during execution
# If any command fails, others still execute (Redis behavior)
```

--------------------------------

### ioredis Connection URL Format (TLS Enabled)

Source: https://upstash.com/docs/redis/troubleshooting/no_auth

This code snippet demonstrates the correct format for connecting to an Upstash Redis database using ioredis with TLS enabled. It highlights the necessity of including the password before the endpoint, separated by a colon.

```text
rediss://:YOUR_PASSWORD@YOUR_ENDPOINT:YOUR_PORT
```

--------------------------------

### Publish and Subscribe to Redis Channels via REST API

Source: https://upstash.com/docs/redis/features/restapi

This snippet illustrates how to use the Upstash REST API for publish-subscribe messaging. The API provides endpoints for publishing messages to a specified channel and subscribing to channels to receive messages. Subscriptions are handled via Server-Sent Events (SSE), delivering messages as 'data:' lines. This enables real-time communication patterns between different clients or services.

```shell
curl -X POST https://us1-merry-cat-32748.upstash.io/subscribe/chat \
  -H "Authorization: Bearer 2553feg6a2d9842h2a0gcdb5f8efe9934" \
  -H "Accept:text/event-stream"
```

```shell
curl -X POST https://us1-merry-cat-32748.upstash.io/publish/chat/hello \
  -H "Authorization: Bearer 2553feg6a2d9842h2a0gcdb5f8efe9934"
```

--------------------------------

### LINSERT Command

Source: https://upstash.com/docs/redis/sdks/ts/commands/list/linsert

Inserts an element before or after a pivot element in a Redis list.

```APIDOC
## LINSERT Command

### Description
Insert an element before or after another element in a list.

### Method
`POST` (or `GET` depending on Redis client implementation for commands)

### Endpoint
`/websites/upstash-redis (or relevant Redis command endpoint)

### Parameters
#### Path Parameters
None

#### Query Parameters
None

#### Request Body
- **key** (string) - Required - The key of the list.
- **direction** (string: `before` | `after`) - Required - Whether to insert the element before or after pivot.
- **pivot** (any) - Required - The element to insert before or after.
- **value** (any) - Required - The element to insert.

### Request Example
```ts
await redis.linsert("key", "before", "b", "x");
```

### Response
#### Success Response (200)
- **integer** (integer) - The list length after insertion, `0` when the list doesn't exist or `-1` when pivot was not found.

#### Response Example
```json
5
```
```
```

