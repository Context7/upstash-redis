Skip to main content
On this page
Upstash Redis is a **highly available, infinitely scalable** Redis-compatible database:
  * 99.99% uptime guarantee with auto-scaling (Prod Pack)
  * Ultra-low latency worldwide
  * Multi-region replication
  * Durable, persistent storage without sacrificing performance
  * Automatic backups
  * Optional SOC-2 compliance, encryption at rest and much more


* * *
## 
​
1. Create an Upstash Redis Database
Once you’re logged in, create a database by clicking `+ Create Database` in the upper right corner. A dialog opens up:
**Database Name:** Enter a name for your database. **Primary Region and Read Regions:** For optimal performance, select the Primary Region closest to where most of your writes will occur. Select the read region(s) where most of your reads will occur. Once you click `Next` and select a plan, your database is running and ready to connect:
* * *
## 
​
2. Connect to Your Database
You can connect to Upstash Redis with any Redis client. For simplicity, we’ll use `redis-cli`. See the Connect Your Client section for connecting via our TypeScript or Python SDKs and other clients. The Redis CLI is included in the official Redis distribution. If you don’t have Redis installed, you can get it here. Connect to your database and execute commands on it:
Copy
Ask AI
```
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

As you run commands, you’ll see updates to your database metrics in (almost) real-time. These database metrics are refreshed every 10 seconds.
Congratulations! You have created an ultra-fast Upstash Redis database! 🎉
**New: Manage Upstash Redis From Cursor (optional)** Manage Upstash Redis databases from Cursor and other AI tools by using our MCP server.
Was this page helpful?
YesNo
Suggest editsRaise issue
Pricing & Limits
⌘I
