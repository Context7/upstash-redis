> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Durable Storage

> This article explains the persistence provided by Upstash databases.

In Upstash, persistence is always enabled, setting it apart from other Redis
offerings. Every write operation is consistently stored in both memory and the
block storage provided by cloud providers, such as AWS's EBS. This dual storage
approach ensures data durability. Read operations are optimized to first check
if the data exists in memory, facilitating faster access. If the data is not in
memory, it is retrieved from disk. This combination of memory and disk storage
in Upstash guarantees reliable data access and maintains data integrity, even
during system restarts or failures.

### Multi Tier Storage

Upstash keeps your data both in memory and disk. This design provides:

* Data safety with persistent storage
* Low latency with in memory access
* Price flexibility by using memory only for active data

In Upstash, an entry in memory is evicted if it remains idle, meaning it has not
been accessed for an extended period. It's important to note that eviction does
not result in data loss since the entry is still stored in the block storage.
When a read operation occurs for an evicted entry, it is efficiently reloaded
from the block storage back into memory, ensuring fast access to the data. This
eviction mechanism in Upstash optimizes memory usage by prioritizing frequently
accessed data while maintaining the ability to retrieve less frequently accessed
data when needed.

<Frame>
  <img src="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/durability/storage.png?fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=c0eeb259e96ff7af442e7448881b59c8" width="600" data-og-width="1201" data-og-height="480" data-path="img/durability/storage.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/durability/storage.png?w=280&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=10610e8264156a1c5de14a81c39012b7 280w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/durability/storage.png?w=560&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=e2d42bfc5b97d7ce53627bdf209358bb 560w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/durability/storage.png?w=840&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=eb172e2fc37ee66a9d0350fafccd4a63 840w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/durability/storage.png?w=1100&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=f39bb49c093c837cd063f185dc79a698 1100w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/durability/storage.png?w=1650&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=2782e0a2cf455b1b9e1f107081d27803 1650w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/durability/storage.png?w=2500&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=5ebefcfbefa685aec3b3d426f7de17a3 2500w" />
</Frame>

<Card title="Can I use Upstash as a database?" icon="lightbulb" iconType="duotone" color="#34D399">
  Definitely, yes. Some users are worried that Redis data will be lost when a
  server crashes. This is not the case for Upstash thanks to Durable Storage.
  Data is reloaded to memory from block storage in case of a server crash.
  Moreover, except for the free tier, all paid tier databases provide extra redundancy by replicating data to multiple instances.
</Card>
