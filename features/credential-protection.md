> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Credential Protection

Enabling Credential Protection ensures your database credentials are never stored within Upstash infrastructure. This enhances security by making credentials accessible only once—at the moment they are generated.

<Note>
  Credential Protection is a [Production
  Pack](/redis/overall/enterprise#prod-pack-features)
  feature.
</Note>

## How It Works

When enabled:

* Redis database credentials are no longer stored in Upstash infrastructure
* Credentials are displayed only once during enablement - save them immediately
* Console features requiring database access are disabled (CLI, Data Browser, Monitor, RBAC)

## Managing Credential Protection

1. Go to database details page → Configuration section
2. Toggle **Protect Credentials** switch:

<Frame>
  <img src="https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/credential-protection/activate-protect-credentials.png?fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=5b7d7f7ee9afb5756a3b4471de204e3b" data-og-width="1940" width="1940" data-og-height="1186" height="1186" data-path="img/credential-protection/activate-protect-credentials.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/credential-protection/activate-protect-credentials.png?w=280&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=aefd3ada4a92b2c7f61ce058d8f02ffe 280w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/credential-protection/activate-protect-credentials.png?w=560&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=0676d401afb66615688c34b00b95cf11 560w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/credential-protection/activate-protect-credentials.png?w=840&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=82e2bd601d002a40cc228e61e8cff64b 840w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/credential-protection/activate-protect-credentials.png?w=1100&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=350b009a0f235561a030dbda20fae342 1100w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/credential-protection/activate-protect-credentials.png?w=1650&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=6f84c61bd72f0e226c586d816eb1f141 1650w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/credential-protection/activate-protect-credentials.png?w=2500&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=00306233061516ee98be27b5ecdfce29 2500w" />
</Frame>

3. Save the credentials shown in the modal:

<Frame>
  <img src="https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/credential-protection/save-credentials.png?fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=eadb65e7235715d1c5a0936f361e9891" data-og-width="1940" width="1940" data-og-height="1186" height="1186" data-path="img/credential-protection/save-credentials.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/credential-protection/save-credentials.png?w=280&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=1c9605add0b9c26038a6f866229320a0 280w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/credential-protection/save-credentials.png?w=560&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=d05000ee37970d2d1bd1f359ae899d24 560w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/credential-protection/save-credentials.png?w=840&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=a6816d547836044aba1e359b3473782b 840w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/credential-protection/save-credentials.png?w=1100&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=8c15437ace32b7c39f1ffe75cec8f730 1100w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/credential-protection/save-credentials.png?w=1650&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=5364abfc3c5851966002b24de873b7e6 1650w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/credential-protection/save-credentials.png?w=2500&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=81ca238de02e2dd4f4c9e23b6e1a2ddc 2500w" />
</Frame>

<Warning>
  Disabling this feature will permanently revoke current credentials and
  generate new ones, potentially breaking applications using those credentials.
</Warning>

## What If You Lose Your Credentials

**Reset Credentials**: This function remains available and, when credential protection is enabled, will generate new protected credentials.

<Frame>
  <img src="https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/credential-protection/reset-credentials.png?fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=4ffe1d18790c44011d0071762aa29dbf" data-og-width="1940" width="1940" data-og-height="1186" height="1186" data-path="img/credential-protection/reset-credentials.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/credential-protection/reset-credentials.png?w=280&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=8fa7381ae952be89f6467d6dd68baf5c 280w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/credential-protection/reset-credentials.png?w=560&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=b1b96c0d34d8d31d18e8b531574615fb 560w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/credential-protection/reset-credentials.png?w=840&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=dc1650393305631314ad49d6fb4f6154 840w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/credential-protection/reset-credentials.png?w=1100&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=bc187b7230cf775b4210fbb855d7a2ad 1100w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/credential-protection/reset-credentials.png?w=1650&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=0298210a8a6fb696b3387f1524fa4fc4 1650w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/credential-protection/reset-credentials.png?w=2500&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=3016bbd6fc57290e0c93ee78feb38525 2500w" />
</Frame>
