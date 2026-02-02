> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Auto Upgrade

By default, Upstash will apply usage limits based on your current plan. When you reach these limits, behavior depends on the specific limit type - bandwidth limits will throttle your traffic, while storage limits will reject new write operations. However, Upstash offers an Auto Upgrade feature that automatically upgrades your database to the next higher plan when you reach your usage limits, ensuring uninterrupted service.

Auto Upgrade is particularly useful for applications with fluctuating or growing workloads, as it prevents service disruptions during high-traffic periods or when your data storage needs expand beyond your current plan. This feature allows your database to automatically scale with your application's demands without requiring manual intervention.

## How Auto Upgrade Works

When enabled:

* For **bandwidth limits**: Instead of throttling your traffic when you reach the bandwidth limit, your database will automatically upgrade to the next plan to accommodate the increased traffic.
* For **storage limits**:
  * **When eviction is off**: Instead of rejecting write operations when you reach maximum data size, your database will upgrade to a plan with larger storage capacity.
  * **When eviction is on**: Your data will be evicted and operations will resume. Auto Upgrade will not be triggered and system will rely on eviction mechanism in this case.

## Managing Auto Upgrade

* You can enable Auto Upgrade by checking the Auto Upgrade checkbox while creating a new database:

  <Frame>
    <img src="https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/auto-upgrade/create-database.png?fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=77910a547dc9bbabe9ee23fde1a6e54a" width="%50" data-og-width="908" data-og-height="1282" data-path="img/auto-upgrade/create-database.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/auto-upgrade/create-database.png?w=280&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=3129a3e3490d16840c059f4b12844d7e 280w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/auto-upgrade/create-database.png?w=560&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=dc9f6faa2689de66edcd4ac6f87ed482 560w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/auto-upgrade/create-database.png?w=840&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=c070e76e2a574304a1938d6934989bc5 840w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/auto-upgrade/create-database.png?w=1100&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=98c8df116e6d16ea6b594269a435546e 1100w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/auto-upgrade/create-database.png?w=1650&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=4b4478c5dbbd1411028a2d1553cd86dc 1650w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/auto-upgrade/create-database.png?w=2500&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=0cf052d33b65104a7399b5321e5cdf06 2500w" />
  </Frame>

* Or for an existing database by clicking Enable in the Configuration/Auto Upgrade box in the database details page:
  <Frame>
    <img src="https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/auto-upgrade/configuration.png?fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=dc1a10f8e4285f3a326852ab2f7e2c35" width="600" height="300" data-og-width="1598" data-og-height="916" data-path="img/auto-upgrade/configuration.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/auto-upgrade/configuration.png?w=280&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=7c1a4f8a08eb4fb8ff726262df3daf99 280w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/auto-upgrade/configuration.png?w=560&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=5a8ff8da59fccf5dba745bde9f670590 560w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/auto-upgrade/configuration.png?w=840&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=3b5c10c4282cbb4008119d74666299a9 840w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/auto-upgrade/configuration.png?w=1100&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=e22ff5287b7ffc7ee7dc84157bb0e7ea 1100w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/auto-upgrade/configuration.png?w=1650&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=ebb37808da50f640d5d3d43f049cfde6 1650w, https://mintcdn.com/upstash/ZVIIe-nWA4-ORRYS/img/auto-upgrade/configuration.png?w=2500&fit=max&auto=format&n=ZVIIe-nWA4-ORRYS&q=85&s=cf7a1c28cfade1a05c162b926fcaa4d2 2500w" />
  </Frame>
