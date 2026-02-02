> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Get Started with Google Cloud Functions

### Prerequisites:

* A GCP account for Google Cloud functions.
* Install [Google Cloud SDK](https://cloud.google.com/sdk/docs/install).
* An Upstash account for Serverless Redis.

### Step 1: Init the Project

* Create a folder, then run `npm init` inside the folder.

### Step 2: Install a Redis Client

Our only dependency is redis client. Install go-redis via `npm install ioredis`

### Step 3: Create a Redis Database

Create a Redis database from Upstash console. **Select the GCP US-Central-1 as
the region.** Free tier should be enough. It is pretty straight forward but if
you need help, check [getting started](../overall/getstarted) guide. In the
database details page, click the Connect button. You will need the endpoint and
password in the next step.

### Step 4: The function Code

Create index.js as below:

```javascript  theme={"system"}
var Redis = require("ioredis");

if (typeof client === "undefined") {
  var client = new Redis("rediss://:YOUR_PASSWORD@YOUR_ENDPOINT:YOUR_PORT");
}

exports.helloGET = async (req, res) => {
  let count = await client.incr("counter");
  res.send("Page view:" + count);
};
```

<Snippet file="redis/ioredisnote.mdx" />

The code simply increments a counter in Redis database and returns its value in
json format.

### Step 5: Deployment

Now we are ready to deploy our API. Deploy via:

```shell  theme={"system"}
gcloud functions deploy helloGET \
--runtime nodejs14 --trigger-http --allow-unauthenticated
```

You will see the URL of your Cloud Function. Click to the URL to check if it is
working properly.

```shell  theme={"system"}
httpsTrigger:
securityLevel: SECURE_OPTIONAL
url: https://us-central1-functions-317005.cloudfunctions.net/helloGET
```

In case of an issue, you can check the logs of your Cloud Function in the GCP
console as below.

<Frame>
  <img src="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/gcp-error.png?fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=99ee8359e129827922ee7a215981bfcf" width="100%" data-og-width="2258" data-og-height="1000" data-path="img/examples/gcp-error.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/gcp-error.png?w=280&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=0af6b90b27aca7cf2899180a35ec1a46 280w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/gcp-error.png?w=560&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=b85aaef2412606c426858201ae8923f2 560w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/gcp-error.png?w=840&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=61b87875712681d9ab30f3f0d40d6ad6 840w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/gcp-error.png?w=1100&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=358eb01f1d5da37a4d23e699d12ae834 1100w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/gcp-error.png?w=1650&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=d1edbe5cea04238b861bc5e2368a4e6b 1650w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/examples/gcp-error.png?w=2500&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=2ec6728a891c7e76179c67a4a4299a24 2500w" />
</Frame>
