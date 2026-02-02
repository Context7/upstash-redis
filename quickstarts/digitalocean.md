> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# DigitalOcean

<Info>
  Upstash has native integration with [DigitalOcean Add-On
  Marketplace](https://marketplace.digitalocean.com/add-ons/upstash-redis).
</Info>

This quickstart shows how to create an Upstash for Redis® Database from
DigitalOcean Add-On Marketplace.

### Database Setup

Creating Upstash for Redis Database requires a DigitalOcean account.

[Login or Sign-up](https://cloud.digitalocean.com/login) for DigitalOcean
account. Then navigate the
[Upstash Redis Marketplace](https://marketplace.digitalocean.com/add-ons/upstash-redis)
page.

Click `Add Upstash Redis` button. Now setup page will open and it will ask
`Database Name / Plan / Region` info.

<Frame>
  <img src="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/digitalocean/img.png?fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=6af99135ba1ea833f64cb26f1943a4eb" data-og-width="708" width="708" data-og-height="1146" height="1146" data-path="img/digitalocean/img.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/digitalocean/img.png?w=280&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=6ed4ff26ddaa40b07fda875b2caeb7ac 280w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/digitalocean/img.png?w=560&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=a4c7a62eadf060b1ec9cabf04a0b389d 560w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/digitalocean/img.png?w=840&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=42cebdbd5a5eb1f36211a929a709daab 840w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/digitalocean/img.png?w=1100&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=47eb6a571658d767986975c338053298 1100w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/digitalocean/img.png?w=1650&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=f5d742fa5939ed1f6b7f96fbaf86845d 1650w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/digitalocean/img.png?w=2500&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=e91e69128c005046f690e6eae534e1cc 2500w" />
</Frame>

After selecting Name, Plan and Region, click `Add Upstash Redis` button.

### Connecting to Database - SSO

After creating database, Overview/Details page will be opened.

Environment variables can be shown in that page.

<Frame>
  <img src="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/digitalocean/img2.png?fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=847d5cd110c5862b287265e8c01d57b4" data-og-width="1672" width="1672" data-og-height="958" height="958" data-path="img/digitalocean/img2.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/digitalocean/img2.png?w=280&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=e425de665cff7bf0fd4c2f029f7c9267 280w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/digitalocean/img2.png?w=560&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=b57d97b5137a14d69a4cbb550d0f7cb4 560w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/digitalocean/img2.png?w=840&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=0ca20e434c3517b6b4838e94405c5e32 840w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/digitalocean/img2.png?w=1100&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=f95c2f88abf309beebe6ebd842d849aa 1100w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/digitalocean/img2.png?w=1650&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=6e672fc905e7e4571ef41c149cb50c1d 1650w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/digitalocean/img2.png?w=2500&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=9683b0651bc6302143c038096c2ee240 2500w" />
</Frame>

While creating a Droplet, Upstash Addon can be selected and environment
variables are automatically injected to Droplet.

These Steps can be followed: `Create --> Droplets --> Marketplace Add-Ons` then
select the previously created Upstash Redis Addon.

<Frame>
  <img src="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/digitalocean/img3.png?fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=4b9dbcc8d1d7e30470669bd4ffc5a012" data-og-width="1638" width="1638" data-og-height="530" height="530" data-path="img/digitalocean/img3.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/digitalocean/img3.png?w=280&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=dd648a113583cff7b9a597a11aea8534 280w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/digitalocean/img3.png?w=560&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=7489cb6e8832b8a649490e9dbd5fcd53 560w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/digitalocean/img3.png?w=840&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=921816a2537bb3d0667478fefa60f2d2 840w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/digitalocean/img3.png?w=1100&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=7c4769fb3ef70cba74f111c3ab2a35f6 1100w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/digitalocean/img3.png?w=1650&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=4a2a8ea0a7de17c350ca49fbf3392835 1650w, https://mintcdn.com/upstash/eu0laKPu7u_-Kw04/img/digitalocean/img3.png?w=2500&fit=max&auto=format&n=eu0laKPu7u_-Kw04&q=85&s=a013c55e1ee2d7174013675a6e51fa1c 2500w" />
</Frame>

Upstash also support Single Sign-On from DigitalOcean to Upstash Console.

So databases created from DigitalOcean can benefit from Upstash Console
features.

In order to access Upstash Console from DigitalOcean just click `Dashboard` link
when you create the Upstash addon.
