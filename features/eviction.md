> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Eviction

By default eviction is disabled, and Upstash Redis will reject write operations once the maximum data size
limit has been reached. However, if you are utilizing Upstash Redis as a cache, you
have the option to enable eviction. Enabling eviction allows older data to be
automatically removed from the cache (including Durable Storage) when the maximum size limit is reached.
This ensures that the cache remains within the allocated size and can make room
for new data to be stored. Enabling eviction is particularly useful when the
cache is intended to store frequently changing or temporary data, allowing the
cache to adapt to evolving data needs while maintaining optimal performance.

* You can enable eviction by checking **Eviction** checkbox while creating a new
  database:

  <Frame>
    <img src="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/eviction/create-database.png?fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=2b8dfc85b0ffbed7aa2e1fa3f50602ab" data-og-width="973" width="973" data-og-height="1062" height="1062" data-path="img/eviction/create-database.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/eviction/create-database.png?w=280&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=130c831abf4194aee46803c1f2183501 280w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/eviction/create-database.png?w=560&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=527c06fce84b35d51c53aeea76e939e3 560w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/eviction/create-database.png?w=840&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=08624f615cf33f68a08b582adf53099f 840w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/eviction/create-database.png?w=1100&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=cca6bf52778637582b3b19a4b9a12db7 1100w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/eviction/create-database.png?w=1650&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=4b26a53edf4b452b782fd573cfaedcf3 1650w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/eviction/create-database.png?w=2500&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=45c723eaac4f6d4c629b4073b2aa0576 2500w" />
  </Frame>

* Or for an existing database by clicking **Enable** in Configuration/Eviction
  box in the database details page:
  <Frame>
    <img src="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/eviction/configuration.png?fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=7239372ec2b89584bc472cb0ea8d8bd0" data-og-width="1984" width="1984" data-og-height="548" height="548" data-path="img/eviction/configuration.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/eviction/configuration.png?w=280&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=03c8de205dc380b5301a6b4b6f97b5af 280w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/eviction/configuration.png?w=560&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=6c61b08ae71acf223bde3b9184f3a891 560w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/eviction/configuration.png?w=840&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=610daaef4953abd382236fe08cbd03ae 840w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/eviction/configuration.png?w=1100&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=db7b98ee0a30569561699a99c0d224b5 1100w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/eviction/configuration.png?w=1650&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=cc78e89b1e11e13b6fa177435bfc96a2 1650w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/eviction/configuration.png?w=2500&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=7b01cad1e942cc3ff04bfd59814e4af9 2500w" />
  </Frame>

Upstash currently uses a single eviction algorithm, called
**optimistic-volatile**, which is a combination of *volatile-random* and
*allkeys-random* eviction policies available in
[the original Redis](https://redis.io/docs/manual/eviction/#eviction-policies).

Initially, Upstash employs random sampling to select keys for eviction, giving
priority to keys marked with a TTL (expire field). If there is a shortage of
volatile keys or they are insufficient to create space, additional non-volatile
keys are randomly chosen for eviction. In future releases, Upstash plans to
introduce more eviction policies, offering users a wider range of options to
customize the eviction behavior according to their specific needs.
