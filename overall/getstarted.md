> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Getting Started

> Create an Upstash Redis database in seconds

Upstash Redis is a **highly available, infinitely scalable** Redis-compatible database:

* 99.99% uptime guarantee with auto-scaling ([Prod Pack](/redis/overall/enterprise#prod-pack-features))
* Ultra-low latency worldwide
* Multi-region replication
* Durable, persistent storage without sacrificing performance
* Automatic backups
* Optional SOC-2 compliance, encryption at rest and much more

***

## 1. Create an Upstash Redis Database

Once you're logged in, create a database by clicking `+ Create Database` in the upper right corner. A dialog opens up:

<Frame>
  <img src="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/create-global.png?fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=09013e74602d754565d828cc90c26aa6" data-og-width="1518" width="1518" data-og-height="977" height="977" data-path="img/getting_started/create-global.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/create-global.png?w=280&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=f1637d9a7924028f57086f27046ec034 280w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/create-global.png?w=560&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=1b215849edb3da0470f4b293164cfbe7 560w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/create-global.png?w=840&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=7167b0f17fd1fb4dbecd1da4ef082313 840w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/create-global.png?w=1100&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=94fccda941b66418a310a4332816e5e3 1100w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/create-global.png?w=1650&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=d730a3da055cd05a25c8cf8daf699610 1650w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/create-global.png?w=2500&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=c9c3886ad67145b0bce8a9cdb167a328 2500w" />
</Frame>

**Database Name:** Enter a name for your database.

**Primary Region and Read Regions:** For optimal performance, select the Primary Region closest to where most of your writes will occur. Select the read region(s) where most of your reads will occur.

Once you click `Next` and select a plan, your database is running and ready to connect:

<Frame>
  <img src="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/database.png?fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=4530264625c10bdf334129ec8b367511" width="100%" data-og-width="1590" data-og-height="1080" data-path="img/getting_started/database.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/database.png?w=280&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=729b8c0843969c86866b06e22747c785 280w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/database.png?w=560&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=d44be677d29134227ff6839fbfc10674 560w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/database.png?w=840&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=414a590eb3c8ed98001a5a781a6268bf 840w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/database.png?w=1100&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=eca30f6532a78f7f25952b41beac50d5 1100w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/database.png?w=1650&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=e60ccc845ab5a2a2b4fb9d66ac0fe948 1650w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/database.png?w=2500&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=b999e96686847b5aeeebc960cf2d5a30 2500w" />
</Frame>

***

## 2. Connect to Your Database

You can connect to Upstash Redis with any Redis client. For simplicity, we'll use `redis-cli`. See the [Connect Your Client](../howto/connectclient) section for connecting via our TypeScript or Python SDKs and other clients.

The Redis CLI is included in the official Redis distribution. If you don't
have Redis installed, you can get it [here](https://redis.io/docs/latest/operate/oss_and_stack/install/install-redis/).

Connect to your database and execute commands on it:

```bash  theme={"system"}
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

As you run commands, you'll see updates to your database metrics in (almost) real-time. These database metrics are refreshed every 10 seconds.

<Frame>
  <img src="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/charts.png?fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=0a226cc212d85606ab415a6a90c66beb" width="100%" data-og-width="1271" data-og-height="279" data-path="img/getting_started/charts.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/charts.png?w=280&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=dc0e463aa9c36746a1694664b239bc45 280w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/charts.png?w=560&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=a61aab0a54b97118d4bc954ea965c522 560w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/charts.png?w=840&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=bb030d544341fdf3081900165d97b10f 840w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/charts.png?w=1100&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=11e42d05b3266a9873b7754ef3727cd0 1100w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/charts.png?w=1650&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=7a571f7865a8effb308e3bab2eeb3875 1650w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/getting_started/charts.png?w=2500&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=79e0053753bf2e716ce274b8a20eb79c 2500w" />
</Frame>

Congratulations! You have created an ultra-fast Upstash Redis database! 🎉

<Check>
  **New: Manage Upstash Redis From Cursor (optional)**

  Manage Upstash Redis databases from Cursor and other AI tools by using our [MCP server](/redis/integrations/mcp).
</Check>
