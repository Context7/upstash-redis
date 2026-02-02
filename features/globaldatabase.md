> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Global Database

In the global database, the replicas are distributed across multiple regions
around the world. The clients are routed to the nearest region. This helps with
minimizing latency for use cases where users can be anywhere in the world.

### Primary Region and Read Regions

The Upstash Global database is structured with a Primary Region and multiple
Read Regions. When a write command is issued, which can be initiated from any region, it is initially sent and processed
at the Primary Region. The write operation is then replicated to all the Read
Regions, ensuring data consistency across the database.

On the other hand, when a read command is executed, it is directed to the
nearest Read Region to optimize response time. By leveraging the Global
database's distributed architecture, read operations can be performed with
reduced latency, as data retrieval occurs from the closest available Read
Region.

The Global database's design thus aids in minimizing read operation latency by
efficiently distributing data across multiple regions and enabling requests to
be processed from the nearest Read Region.

User selects a single primary region and multiple read regions. For the best
performance, you should select the primary region in the same location where
your writes happen. Select the read regions where your clients that read the
Redis located. You may have your database with a single primary region but no
read regions which would be practically same with a single region (regional)
database. You can add or remove regions on a running Redis database.

Here the list of regions currently supported:

<Tabs>
  <Tab title="Amazon Web Services">
    | Region                  | Code           |
    | ----------------------- | -------------- |
    | N. Virginia, USA        | us-east-1      |
    | Ohio, USA               | us-east-2      |
    | N. California, USA      | us-west-1      |
    | Oregon, USA             | us-west-2      |
    | Central Canada          | ca-central-1   |
    | Sao Paulo, Brazil       | sa-east-1      |
    | Ireland                 | eu-west-1      |
    | London, UK              | eu-west-2      |
    | Frankfurt, Germany      | eu-central-1   |
    | Mumbai, India           | ap-south-1     |
    | Singapore               | ap-southeast-1 |
    | Tokyo, Japan            | ap-northeast-1 |
    | Sydney, Australia       | ap-southeast-2 |
    | Cape Town, South Africa | af-south-1     |
  </Tab>

  <Tab title="Google Cloud Platform">
    | Region        | Code            |
    | ------------- | --------------- |
    | Iowa, USA     | us-central1     |
    | Virginia, USA | us-east4        |
    | Belgium       | europe-west1    |
    | Tokyo, Japan  | asia-northeast1 |
  </Tab>
</Tabs>

<Frame>
  <img src="https://mintcdn.com/upstash/gdRdyWQoqxKV6AH0/img/globaldb/regionselect.png?fit=max&auto=format&n=gdRdyWQoqxKV6AH0&q=85&s=67a7e9ff8cd616c3c4cc442e83c5e0d6" width="520" data-og-width="1086" data-og-height="1436" data-path="img/globaldb/regionselect.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/gdRdyWQoqxKV6AH0/img/globaldb/regionselect.png?w=280&fit=max&auto=format&n=gdRdyWQoqxKV6AH0&q=85&s=d5d51451dab7f1f7dfe041786c1eb8c9 280w, https://mintcdn.com/upstash/gdRdyWQoqxKV6AH0/img/globaldb/regionselect.png?w=560&fit=max&auto=format&n=gdRdyWQoqxKV6AH0&q=85&s=f27dddda2c1a69d56e86db664a7f7be0 560w, https://mintcdn.com/upstash/gdRdyWQoqxKV6AH0/img/globaldb/regionselect.png?w=840&fit=max&auto=format&n=gdRdyWQoqxKV6AH0&q=85&s=30f46be40941991ae5f680d45a3ddf3d 840w, https://mintcdn.com/upstash/gdRdyWQoqxKV6AH0/img/globaldb/regionselect.png?w=1100&fit=max&auto=format&n=gdRdyWQoqxKV6AH0&q=85&s=3fbb0d3e30e17ef1ba87ab47e9dd01dc 1100w, https://mintcdn.com/upstash/gdRdyWQoqxKV6AH0/img/globaldb/regionselect.png?w=1650&fit=max&auto=format&n=gdRdyWQoqxKV6AH0&q=85&s=385d4934039373d8d9a932308add8ba4 1650w, https://mintcdn.com/upstash/gdRdyWQoqxKV6AH0/img/globaldb/regionselect.png?w=2500&fit=max&auto=format&n=gdRdyWQoqxKV6AH0&q=85&s=414219db3b3f9c17d47f44f4b5e5ce04 2500w" />
</Frame>

In our internal tests, we see the following latencies (99th percentile):

* Read latency from the same region \<1ms
* Write latency from the same region \<5ms
* Read/write latency from the same continent \<50ms

<Frame>
  <img src="https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/globaldb/map2.png?fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=6e744968e9185a825f52ee2986a23f7e" width="1000" data-og-width="1680" data-og-height="874" data-path="img/globaldb/map2.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/globaldb/map2.png?w=280&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=3f9b8524ff479b37266efe47da799185 280w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/globaldb/map2.png?w=560&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=a47f9e8c867f53df998e390d09866fa9 560w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/globaldb/map2.png?w=840&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=e5ea157ad2d54c6ce0ac0a2636861eae 840w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/globaldb/map2.png?w=1100&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=da93e8b5bdf527ee2e54ea6fcc32f8e5 1100w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/globaldb/map2.png?w=1650&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=0218a1971423ae33cfc9500ae0aaa1dc 1650w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/globaldb/map2.png?w=2500&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=966b9f9e1835f38321b8c1c879b50df3 2500w" />
</Frame>

### Architecture

In the multi region architecture, each key is owned by a primary replica which
is located at the region that you choose as primary region. Read replicas become
the backups of the primary for the related keys. The primary replica processes
the writes, then propagates them to the read replicas. Read requests are
processed by all replicas, this means you can read a value from any of the
replicas. This model gives a better write consistency and read scalability.

Each replica employs a failure detector to track the liveness of the primary
replica. When the primary replica fails for a reason, read replicas start a new
leader election round and elect a new leader (primary). This is the only
unavailability window for the cluster where your requests can be blocked for a
short period of time.

<Note>
  Global Database is designed to optimize the latency of READ operations. It may
  not be a good choice if your use case is WRITE heavy.
</Note>

### Use Cases

* **Edge functions:** Edge computing (Cloudflare workers, Fastly Compute) is
  becoming a popular way of building globally fast applications. But there are
  limited data solutions accessible from edge functions. Upstash Global Database
  is accessible from Edge functions with the REST API. Low latency from all edge
  locations makes it a perfect solution for Edge functions

* Multi region serverless architectures: You can run your AWS Lambda function in
  multiple regions to lower global latency. Vercel/Netlify functions can be run
  in different regions. Upstash Global database provides low latency data
  wherever your serverless functions are.

* Web/mobile use cases where you need low latency globally. Thanks to the read
  only REST API, you can access Redis from your web/mobile application directly.
  In such a case, Global Database will help to lower the latency as you can
  expect the clients from anywhere.

### High Availability and Disaster Recovery

Although the main motivation behind the Global Database is to provide low
latency; it also makes your database resilient to region wide failures. When a
region is not available, your requests are routed to another region; so your
database remains available.

### Consistency

Global Database is an eventually consistent database. The write request returns
after the primary replica processes the operation. Write operation is replicated
to read replicas asynchronously. Read requests can be served by any replica,
which gives better horizontal scalability but also means a read request may
return a stale value while a write operation for the same key is being
propagated to read replicas.

In case of cluster wide failures like network partitioning (split brain);
periodically running anti entropy jobs resolve the conflicts using LWW
algorithms and converge the replicas to the same state.

### Upgrade from Regional to Global

Currently, we do not support auto-upgrade from regional to global database. You
can export data from your old database and import into the global database.

### Pricing

Global Database charges \$0.2 per 100K commands. The write commands are replicated to all read regions in addition to primary region so the replications are counted as commands. For example, if you have 1 primary 1 read region, 100K writes will cost \$0.4 (\$0.2 x 2). You can use Global Database in the free tier too. Free usage is limited with max one read region.
