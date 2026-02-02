> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Backup/Restore

You can create backups of your Redis database and restore them when needed. Backups allow you to preserve your data and recover it to any database in your account or team.

## Creating a Backup

<Info>
  During a backup operation, certain administrative operations will be temporarily unavailable: Backup operations, database config changes, plan and region setup, transferring database.
  Regular Redis commands (GET, SET, etc.) are not blocked and continue to work normally.
</Info>

There are two ways to create a backup of your database:

### Create an Immediate Backup

To create a backup right now:

* Go to the database details page and navigate to the `Backups` tab
* Click on the `Backup & Export` button
* Choose `Backup`

<Frame>
  <img src="https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/backup-export-button.png?fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=88c7cb7acbfb3e3cb74493bfa22bfa41" width="800" data-og-width="2420" data-og-height="1582" data-path="img/backuprestore/backup-export-button.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/backup-export-button.png?w=280&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=7fa36e4e3801a6eed5cbdc679b6cfe4e 280w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/backup-export-button.png?w=560&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=d2225b053f20d191483d5dc7ed33fd89 560w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/backup-export-button.png?w=840&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=d66a53796f3a9a88e0f8aabbbae5e631 840w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/backup-export-button.png?w=1100&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=fd41d3a07df23097645cd9e4fd5e2804 1100w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/backup-export-button.png?w=1650&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=d19e9116ae9d51b133caefafbdeca3f6 1650w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/backup-export-button.png?w=2500&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=48ca56b0611d535044d45b66a51adba9 2500w" />
</Frame>

Backup process will start and will appear in the backups table below.

### Schedule Periodic Backups

To automatically create backups on a regular schedule:

* Go to the database details page and navigate to the `Backups` tab
* Click the switch next to `Daily Backup` to enable daily backup or click on `Daily Backup` text itself to select how long the backup is to be stored (1 or 3 days)

<Frame>
  <img src="https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/daily-backup-toggle.png?fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=d1acf0417ed2eb56a47f3070eb81b67f" width="800" data-og-width="2420" data-og-height="1258" data-path="img/backuprestore/daily-backup-toggle.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/daily-backup-toggle.png?w=280&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=58cdc80cd75bc37e84cce90afd2e93b0 280w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/daily-backup-toggle.png?w=560&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=06b3b298ebf87df7c1aa8b443f00fe09 560w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/daily-backup-toggle.png?w=840&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=a971638e46e00b71f05609d2fc91c64b 840w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/daily-backup-toggle.png?w=1100&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=de9ff9de03381a865e33ced86fbb35b5 1100w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/daily-backup-toggle.png?w=1650&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=d2c80ca4f9e12ea47b454eed79a285c7 1650w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/daily-backup-toggle.png?w=2500&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=5a36731e89e8472097df882e8d298b59 2500w" />
</Frame>

With daily backups enabled, your database will be automatically backed up every day.

### Managing Backups

All created backups are displayed in the backups table in the `Backups` tab. From this table, you can:

* View backup details (name, creation date, size)
* Restore your database from any backup
* Delete backups you no longer need

## Restoring from Backup

<Warning>
  All existing data in the target database will be deleted before the restore operation begins.
</Warning>

You can restore your database from any backup in your account or team.

### Restore from the Backups Table

To restore from a backup of the current database:

* Go to the database details page and navigate to the `Backups` tab
* Find the backup you want to restore in the backups table
* Click on the `Restore` button next to the backup
* Confirm that you are deleting existing data and want to proceed with the restore

<Frame>
  <img src="https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/restore-from-table.png?fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=93a376068dae5549902766dbd104b27a" width="800" data-og-width="2420" data-og-height="1090" data-path="img/backuprestore/restore-from-table.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/restore-from-table.png?w=280&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=6730e6036a61494b6d23d838375d2041 280w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/restore-from-table.png?w=560&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=0003acdcaa1cf0e76649f9208616bf31 560w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/restore-from-table.png?w=840&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=f493a846a3faf712d68f7d34763bb085 840w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/restore-from-table.png?w=1100&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=e443b39c4685b1694d1d6143ccdea5b1 1100w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/restore-from-table.png?w=1650&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=80e441acb6c351c4da1bdd1d5aec522d 1650w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/restore-from-table.png?w=2500&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=c6095731d338d9bcd908d0202a6d9345 2500w" />
</Frame>

### Restore from Any Database Backup

To restore from a backup created from any database in your account or team:

* Go to the database details page and navigate to the `Backups` tab
* Click on the `Restore...` button
* Select the source database (the database from which the backup was created)
* Select the backup you want to restore
* Click on `Start Restore`

<Frame>
  <img src="https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/restore-modal.png?fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=4e951472a9870132c3505e9723c41bb8" width="700" data-og-width="2420" data-og-height="1556" data-path="img/backuprestore/restore-modal.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/restore-modal.png?w=280&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=0d91674aca76903ad58cc32f95604e9b 280w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/restore-modal.png?w=560&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=06e903aa588e96f6276cbd2a7cf5ac2f 560w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/restore-modal.png?w=840&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=d145d5ca8fdc7c69bea373c1c67b2f0a 840w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/restore-modal.png?w=1100&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=29d35262023e83589e94c2aeff7458d0 1100w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/restore-modal.png?w=1650&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=ed0d3c3fef066f81ebe0c9e8e456405d 1650w, https://mintcdn.com/upstash/xtCO9hUjtzDjszw3/img/backuprestore/restore-modal.png?w=2500&fit=max&auto=format&n=xtCO9hUjtzDjszw3&q=85&s=1253397e349af66bae4aeb8c9aba4022 2500w" />
</Frame>

### Restore from the Redis List Page

You can also restore databases directly from the Redis list page. This method is explained in detail in the [Import/Export documentation](/redis/howto/importexport).
