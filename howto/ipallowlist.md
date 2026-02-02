> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Use IP Allowlist

<Info>
  IP Allowlist is available on all plans except for the free plan.
</Info>

IP Allowlist can be used to restrict which IP addresses are permitted to access your database by comparing a connection's address with predefined CIDR blocks. This feature enhances database security by allowing connections only from specified IP addresses. For example if you have dedicated production servers with static IP addresses, enabling IP allowlist blocks connections from other addresses.

<img src="https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/ipallowlist/ipallowlist.png?fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=fe7461f8b0bed3087379e89050101dbe" alt="allowlist" data-og-width="1930" width="1930" data-og-height="264" height="264" data-path="img/ipallowlist/ipallowlist.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/ipallowlist/ipallowlist.png?w=280&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=eba035250fb240a609d516152ed6e618 280w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/ipallowlist/ipallowlist.png?w=560&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=c175125f56e9399ee399e560984bb911 560w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/ipallowlist/ipallowlist.png?w=840&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=690f622144438db97854fb053977b106 840w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/ipallowlist/ipallowlist.png?w=1100&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=ddf7573ae788a4816cf6a9a699d46819 1100w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/ipallowlist/ipallowlist.png?w=1650&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=48156fae282cf2bcdf4d2a974d25ad96 1650w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/ipallowlist/ipallowlist.png?w=2500&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=a56d6cd2b3ee29c04ea39eaf01c90b7e 2500w" />

## Enabling IP Allowlist

By default, any IP address can be used to connect to your database. You must add at least one IP range to enable the allowlist. You can manage added IP ranges in the `Configuration` section on the database details page. You can either provide

* IPv4 address, e.g. `37.237.15.43`
* CIDR block, e.g. `181.49.172.0/24`

<Info>
  Currently, IP Allowlist only supports IPv4 addresses.
</Info>

You can use more than one range to allow multiple clients. Meeting the criteria of just one is enough to establish a connection.

<Note>
  It may take a few minutes for changes to propagate.
</Note>
