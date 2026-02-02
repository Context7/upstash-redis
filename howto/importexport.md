> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Import/Export Data

## Importing Data

You can import data into your Upstash Redis database from two sources: an existing backup or an RDB file.

<Warning>
  All existing data in the target database will be deleted before the import operation begins.
</Warning>

### Start an Import

To begin importing data:

* Go to the [Redis database list page](https://console.upstash.com/redis) in the Upstash console
* Click on the `Import...` button

<Frame>
  <img src="https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/import-button.png?fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=9ea9d10c6de7b577101c9baadfcea0e6" width="800" data-og-width="2420" data-og-height="1320" data-path="img/backuprestore/import-button.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/import-button.png?w=280&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=4b91368ae50ae44931f96f1e04a33aa2 280w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/import-button.png?w=560&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=de8583c8bf76222e307bfd7104e3952e 560w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/import-button.png?w=840&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=0955b6c9dd6a6017cdb84051e6a91f70 840w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/import-button.png?w=1100&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=2fb10bfeb1d0eaaddc20176b696c9713 1100w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/import-button.png?w=1650&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=be813557667120f87cbe871932b980e7 1650w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/import-button.png?w=2500&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=248cf0c0a863ad1ae7712a54d8bab284 2500w" />
</Frame>

You'll see a dialog with two import options:

### Option 1: Import from Backup

Import data from a backup of any existing database in your account or team:

* Select `From Backup` as the source
* Choose the source database (the database from which the backup was created)
* Select the backup you want to import from
* Select the target database (the database you want to import into)
* Click `Start Import`

<Frame>
  <img src="https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/import-from-backup.png?fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=ab2b67d735f928d945bce60078143350" width="700" data-og-width="2420" data-og-height="1476" data-path="img/backuprestore/import-from-backup.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/import-from-backup.png?w=280&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=dbb1ae7c2f6f275d382113b7ed979fc0 280w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/import-from-backup.png?w=560&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=7bb26b2c78311dde7de3e16771652565 560w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/import-from-backup.png?w=840&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=775b75c227abb8655e7e012ea162a968 840w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/import-from-backup.png?w=1100&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=c9b938a839eb3c93ec167664d260efee 1100w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/import-from-backup.png?w=1650&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=2ca883d39a16fe6e9d1d1d9411fa5645 1650w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/import-from-backup.png?w=2500&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=f70701f881dce5d8ec9e5eb5a9913862 2500w" />
</Frame>

### Option 2: Import from RDB File

Import data from an external Redis database by uploading an RDB file:

* Select `From RDB File` as the source
* Click `Upload RDB File` and select your RDB file
* Select the target database (the database you want to import into)
* Click `Start Import`

<Frame>
  <img src="https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/import-from-rdb.png?fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=b337a4b4a8dc314e604f802604dfc5be" width="700" data-og-width="2420" data-og-height="1528" data-path="img/backuprestore/import-from-rdb.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/import-from-rdb.png?w=280&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=a551ff9f20c8753d9f64068d9ee40911 280w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/import-from-rdb.png?w=560&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=e45d941be5e2e63ec0b5522f5e2eeebd 560w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/import-from-rdb.png?w=840&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=a0c29747cc31eb1364620fbbad09912b 840w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/import-from-rdb.png?w=1100&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=3ed5b6ee07b717d25efc57f84b48e0c1 1100w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/import-from-rdb.png?w=1650&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=b6340832f418c49e50f0bd681821dccf 1650w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/import-from-rdb.png?w=2500&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=6c2a1b0d710b7e32b57ff508ab927ecb 2500w" />
</Frame>

<Info>
  If you're importing from an external Redis database (from another provider or on-premise), you'll need to export it as an RDB file first.
</Info>

## Exporting Data

<Warning>
  **Coming Soon**: The export feature is not yet available but will be released soon. The following documentation describes how it will work.
</Warning>

You'll be able to export your Upstash Redis database as an RDB file for backup or migration purposes.

### Request an Export

To export your database:

* Go to the database details page and navigate to the `Backups` tab
* Click on the `Backup & Export` button
* Choose `Export`

<Frame>
  <img src="https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/export-button.png?fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=ab971ba2b65211303a596b4174fb6ff9" width="800" data-og-width="2420" data-og-height="1468" data-path="img/backuprestore/export-button.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/export-button.png?w=280&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=caad4098e706adeee525d0bbdad7d28f 280w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/export-button.png?w=560&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=94da04098ca649f0d27e91252e11d575 560w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/export-button.png?w=840&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=6de504084662f5e76ab7515537767508 840w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/export-button.png?w=1100&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=4545b332d775f4e284067153dfae63e5 1100w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/export-button.png?w=1650&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=abf23a654a8df4b0b8100c7dc91e06cd 1650w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/export-button.png?w=2500&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=cbeb7f26bbb0ca0f2dcf71988f73e0dd 2500w" />
</Frame>

Your database will be exported as an RDB file. Once you start the export, you'll see the export progress in the backups table.

### Download Your Export

Once the export completes, you'll see a `Download` button in the backups table:

* Find your export in the backups table
* Click the `Download` button to download the RDB file

<Info>
  Not all Redis data structures are included in RDB exports. Notably, Redis Functions data will not be available in the export.
</Info>
