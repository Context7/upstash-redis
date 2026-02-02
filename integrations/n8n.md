> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# n8n with Upstash Redis

## Quickstart

In this quickstart we're going to set up an Redis node in n8n using Upstash Redis, and go over an example use case step by step.

***

### Step 1: Get Your Upstash Redis Credentials

1. Go to Upstash Console and create a Redis database if you don't have any
2. Note down your credentials in the details page, we will be using those to connect Redis
   Node in n8n to our Upstash Redis instance.
   <img src="https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-credentials.png?fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=293c28caa72112f9bc65bd47286fb998" data-og-width="1296" width="1296" data-og-height="1002" height="1002" data-path="img/n8n/redis-credentials.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-credentials.png?w=280&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=558de513f4db32937abd719b2d97c702 280w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-credentials.png?w=560&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=a8109e271366d915e72906b7a836b19f 560w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-credentials.png?w=840&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=1097bc6589a8b04515896108836ae6f2 840w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-credentials.png?w=1100&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=f98c42f3d7f6206f3c0f9342d87a2f19 1100w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-credentials.png?w=1650&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=18a59c02bedc67e50ca243ec0dc2d058 1650w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-credentials.png?w=2500&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=935e03368d2cd43c6d4a7cd84b6c38c0 2500w" />

***

### Step 2: Set Up an n8n Project

1. Go to [https://n8n.io](https://n8n.io) and create a new project
2. Create a Trigger as Webhook with default settings, this will be our entry point. Our Redis instances gonna watch the visits to this url.
   <img src="https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/webhook.png?fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=46fccbccd381de6cb7a4e7a6238a2395" data-og-width="1940" width="1940" data-og-height="1044" height="1044" data-path="img/n8n/webhook.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/webhook.png?w=280&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=2840fcb0514aa9fd29904c3b86b02787 280w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/webhook.png?w=560&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=ee46e8d40b539cdd0f8628d313f54e9f 560w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/webhook.png?w=840&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=aa5a727dc846da79fa3b05d66c6eb735 840w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/webhook.png?w=1100&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=2fad07185afd20ec5f627fdc73d79f0d 1100w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/webhook.png?w=1650&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=d1e6aef67c2c704d11eba58c510b3f34 1650w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/webhook.png?w=2500&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=693cd81b6f8a6cec7effdf0656e55a69 2500w" />

***

### Step 3: Create a Redis Node

Now, Let's create a redis node and connect it to our Upstash Redis instance

1. Search for redis in nodes, and select increment action.
   <img src="https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-1.png?fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=17210dc691c9727719aa8b2e7c13b4b7" data-og-width="1940" width="1940" data-og-height="1108" height="1108" data-path="img/n8n/redis-1.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-1.png?w=280&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=21305ab4e1b3692fefb541a0604495d9 280w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-1.png?w=560&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=f57b6f819de738965a8fdb742050df1b 560w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-1.png?w=840&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=a253417c3efe88098458545bc68aa585 840w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-1.png?w=1100&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=623227d90c713d2d9d9a75150055fb9b 1100w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-1.png?w=1650&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=50114b2ab0c1525d8b48bcefdd179169 1650w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-1.png?w=2500&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=fa1517308989617be05d84342627372a 2500w" />

2. In the opening window, click select credentials, and create new credentials.
   Later, for other redis nodes, this will be saved and used automatically.
   <img src="https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-2.png?fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=5886973b53daaa61f2ce68d22ed582ce" data-og-width="1940" width="1940" data-og-height="1184" height="1184" data-path="img/n8n/redis-2.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-2.png?w=280&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=05e58e83a42231e959ef4547e3cc428d 280w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-2.png?w=560&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=59890df027b5f472179be691f73f5b8e 560w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-2.png?w=840&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=ad7e1a1730fb4c61ca6de0ce8c8dba51 840w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-2.png?w=1100&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=54b8704f321571db05ee7156f8c89151 1100w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-2.png?w=1650&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=71955838f50775c68c6eb2148fe521f0 1650w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-2.png?w=2500&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=914f51b4f4fe8b3721be51db7dbfd855 2500w" />

3. Fill the credentials.

   * Pass your Upstash Token to the password field.
   * Leave the user field blank
   * Pass your Upstash Redis endpoint to the host field. (Leave the https\:// part out)
   * If your Upstash Database has a port other than the default 6379, change it here.

   <img src="https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-3.png?fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=b70059ad2814d8247382d5b7c85771ff" data-og-width="1940" width="1940" data-og-height="1182" height="1182" data-path="img/n8n/redis-3.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-3.png?w=280&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=bb5523fa801bdfda785eebf717d3f606 280w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-3.png?w=560&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=93c9b80e7157395d87a7c960e636df83 560w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-3.png?w=840&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=55f4036c037979c91000bc0cbae329fd 840w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-3.png?w=1100&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=14cd77f09755336c19a2c09b3fb958e1 1100w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-3.png?w=1650&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=cec94da1a6bc7c5df368fad08fa9c086 1650w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-3.png?w=2500&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=56eeaab28cfcb05d27891dee4cb65fa2 2500w" />

4. Enable SSL (Upstash Redis requires SSL) and hit the save button.
   <img src="https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-4.png?fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=4fa61b1766a9660896b4cd006bee3998" data-og-width="1940" width="1940" data-og-height="1182" height="1182" data-path="img/n8n/redis-4.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-4.png?w=280&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=939c1ef664e333602e1764bcdb81f6c4 280w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-4.png?w=560&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=04bc388586ad1e1e0080b44b54355c25 560w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-4.png?w=840&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=8468e6d6949182c03a4fd294c399c0b3 840w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-4.png?w=1100&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=718757ed3bc098a8287370a6de3d0177 1100w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-4.png?w=1650&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=2fd733d5ee8eb57a607a565f0b54c836 1650w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-4.png?w=2500&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=92909303daedb6d2f78e196be3ae4dcb 2500w" />

***

### Redis Example: Store the Visit Count per Visitor

1. Track the users with `x-real-ip`
   <img src="https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-increment.png?fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=9eee362c716758f14a5708525ab7f67f" data-og-width="1162" width="1162" data-og-height="716" height="716" data-path="img/n8n/redis-increment.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-increment.png?w=280&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=85e7d6d505fbe16a0b78a0fcf7ec4285 280w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-increment.png?w=560&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=1e21288675aa6dab3a067471ad8732fc 560w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-increment.png?w=840&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=3134cd19f6b5a6e5728152a029f8c4c2 840w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-increment.png?w=1100&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=db3efceea20d032531f7c17ddc45f2b4 1100w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-increment.png?w=1650&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=9cc48d9c586b374163085a75611429c2 1650w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-increment.png?w=2500&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=5a777218e790e7c15b5efa31298d7a58 2500w" />
2. Add another redis node with get action to see the visit counts
   <img src="https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-get.png?fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=42249a3617a1789a5b42cdf83f585473" data-og-width="1940" width="1940" data-og-height="1108" height="1108" data-path="img/n8n/redis-get.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-get.png?w=280&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=8cdf12062830a80ac6dc665d4118d94b 280w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-get.png?w=560&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=04d246258e3c28eff823ca4faf9b21b2 560w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-get.png?w=840&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=8b9a184ea20f41b9d5c021cddcc134d5 840w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-get.png?w=1100&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=ed89e1917c8f8446998b1a36ff0b6255 1100w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-get.png?w=1650&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=d3723e58a01a7ac24dc6af8308c937cc 1650w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-get.png?w=2500&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=c56ef7f7cb15950c7d5cec6e48d54afb 2500w" />
3. Read the set visit count with redis get
   <img src="https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-get-2.png?fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=adae35c65316e902112286724d772b89" data-og-width="1940" width="1940" data-og-height="1572" height="1572" data-path="img/n8n/redis-get-2.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-get-2.png?w=280&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=5a61abf209a3346e5e48cf3c5e8b1d3c 280w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-get-2.png?w=560&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=9947b2f77fdab58cb6122fb74acaf840 560w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-get-2.png?w=840&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=f444307a7ac571c1571ea28605713d7f 840w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-get-2.png?w=1100&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=2ed4d47c1a155f4e1da4878c734ae96e 1100w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-get-2.png?w=1650&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=7967dd19ed0eb118119256149b0a89d9 1650w, https://mintcdn.com/upstash/H3SBHpRUOHZbOxSA/img/n8n/redis-get-2.png?w=2500&fit=max&auto=format&n=H3SBHpRUOHZbOxSA&q=85&s=42c0266758d3ce668174507bf0ae7683 2500w" />

***

### Test Redis Example

Run the workflow and visit the webhook URL, This will send a get request and trigger the workflow run.
Then from the headers your ip will be fetched and in the redis instance you will see `user:user-ip` set to `1`.
As you visit the page it will be incremented and at the end of the workflow you can track and confirm this setup with
the get request.

***
