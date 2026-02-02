> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Integration with Third Parties & Partnerships

<Frame>
  <img height="100" src="https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/integration/upstash-integration-diagram.png?fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=12b02067fd6101b2b40df79848f845f4" data-og-width="1912" data-og-height="1570" data-path="img/integration/upstash-integration-diagram.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/integration/upstash-integration-diagram.png?w=280&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=1a1eaa2be7331d3ccb3fec182c7d85c7 280w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/integration/upstash-integration-diagram.png?w=560&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=ce655b76b595e01c3639ceb3ceaeab34 560w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/integration/upstash-integration-diagram.png?w=840&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=3ead270c9c90e142fa00987dab2efb83 840w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/integration/upstash-integration-diagram.png?w=1100&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=5821438d41e99e22447a29ec6d891889 1100w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/integration/upstash-integration-diagram.png?w=1650&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=1fe4a7a092250af25b26086c22a888fa 1650w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/integration/upstash-integration-diagram.png?w=2500&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=bdf82bf103f38088843b890fb776a5e5 2500w" />
</Frame>

## Introduction

In this guideline we will outline the steps to integrate Upstash into your platform (GUI or Web App) and allow your users to create and manage Upstash databases without leaving your interfaces. We will explain how to use OAuth2.0 as the underlying foundation to enable this access seamlessly.

If your product or service offering utilizes Redis, Vector or QStash or if there is a common use case that your end users enable by leveraging these database resources, we invite you to be a partner with us. By integrating Upstash into your platform, you can offer a more complete package for your customers and become a one stop shop. This will also position yourself at the forefront of innovative cloud computing trends such as serverless and expand your customer base.

This is the most commonly used partnership integration model that can be easily implemented by following this guideline. Recently [Cloudflare workers integration](https://blog.cloudflare.com/cloudflare-workers-database-integration-with-upstash/) is implemented through this methodology. For any further questions or partnership discussions please send us an email at [partnerships@upstash.com](mailto:partnerships@upstash.com)

<Info>
  Before starting development to integrate Upstash into your product, please
  send an email to [partnerships@upstash.com](mailto:partnerships@upstash.com) for further assistance and guidance.
</Info>

**General Flow (High level user flow)**

1. User clicks **`Connect Upstash`** button on your platform’s surface (GUI, Web App)
2. This initiates the OAuth 2.0 flow, which opens a new browser page displaying the **`Upstash Login Page`**.
3. If this is an existing user, user logins with their Upstash credentials otherwise they can directly sign up for a new Upstash account.
4. Browser window redirects to **`Your account has been connected`** page and authentication window automatically closes.
5. After the user returns to your interface, they see their Upstash Account is now connected.

## Technical Design (SPA - Regular Web Application)

1. Users click `Connect Upstash` button from Web App.
2. Web App initiate Upstash OAuth 2.0 flow. Web App can use
   [Auth0 native libraries](https://auth0.com/docs/libraries).

<Note>
  Please reach [partnerships@upstash.com](mailto:partnerships@upstash.com) to receive client id and callback url.
</Note>

3. After user returns from OAuth 2.0 flow then web app will have JWT token. Web
   App can generate Developer Api key:

```bash  theme={"system"}
curl -XPOST https://api.upstash.com/apikey \
    -H "Authorization: Bearer JWT_KEY" \
    -H "Content-Type: application/json" \
    -d '{ "name": "APPNAME_API_KEY_TIMESTAMP" }'
```

4. Web App need to save Developer Api Key to the backend.

## Technical Design ( GUI Apps )

<Frame>
  <img src="https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/integration/oauth2-integration.png?fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=bcef33147cd866b6e5491aae3b051b3f" data-og-width="2226" width="2226" data-og-height="1692" height="1692" data-path="img/integration/oauth2-integration.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/integration/oauth2-integration.png?w=280&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=e006a10cd79f12d80e3e13dd0f22a7fe 280w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/integration/oauth2-integration.png?w=560&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=0868fc8d69400942bcccb568131be41b 560w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/integration/oauth2-integration.png?w=840&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=fd2fa7c5719b0949f13f2fa972f1d5fb 840w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/integration/oauth2-integration.png?w=1100&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=32f6c33468107be0126cb5e92d0b9f34 1100w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/integration/oauth2-integration.png?w=1650&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=2be1b63bccc956937c20d79bb5eee6d1 1650w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/integration/oauth2-integration.png?w=2500&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=331dbabdd4c875ecfbddc94eebba1152 2500w" />
</Frame>

1. User clicks **`Connect Upstash`** button from web app.
2. Web app initiates Upstash OAuth 2.0 flow and it can use **[Auth0 native libraries](https://auth0.com/docs/libraries)**.
3. App will open new browser:

```
https://auth.upstash.com/authorize?response_type=code&audience=upstash-api&scope=offline_access&client_id=XXXXXXXXXX&redirect_uri=http%3A%2F%2Flocalhost:3000
```

<Note>Please reach [partnerships@upstash.com](mailto:partnerships@upstash.com) to receive client id.</Note>

4. After user authenticated Auth0 will redirect user to
   `localhost:3000/?code=XXXXXX`

5. APP can return some nice html response when Auth0 returns to `localhost:3000`

6. After getting `code` parameter from the URL query, GUI App will make http
   call to the Auth0 code exchange api. Example CURL request

```bash  theme={"system"}
curl -XPOST 'https://auth.upstash.com/oauth/token' \
  --header 'content-type: application/x-www-form-urlencoded' \
  --data 'grant_type=authorization_code --data audience=upstash-api' \
  --data 'client_id=XXXXXXXXXXX' \
  --data 'code=XXXXXXXXXXXX' \
  --data 'redirect_uri=localhost:3000'
```

Response:

```json  theme={"system"}
{
  "access_token": "XXXXXXXXXX",
  "refresh_token": "XXXXXXXXXXX",
  "scope": "offline_access",
  "expires_in": 172800,
  "token_type": "Bearer"
}
```

7. After 6th Step the response will include `access_token`, it has 3 days TTL.
   GUI App will call Upstash API to get a developer api key:

```bash  theme={"system"}
curl https://api.upstash.com/apikey -H "Authorization: Bearer JWT_KEY" -d '{ "name" : "APPNAME_API_KEY_TIMESTAMP" }'
```

8. GUI App will save Developer Api key locally. Then GUI App can call any
   Upstash Developer API [developer.upstash.com/](https://developer.upstash.com/)

## Managing Resources

After obtaining Upstash Developer Api key, your platform surface (web or GUI) can call Upstash API. For example **[Create Database](https://developer.upstash.com/#create-database-global)**, **[List Database](https://developer.upstash.com/#list-databases)**

In this flow, you can ask users for region information and name of the database then can call Create Database API to complete the task

Example CURL request:

```bash  theme={"system"}
curl -X POST \
  https://api.upstash.com/v2/redis/database \
  -u 'EMAIL:API_KEY' \
  -d '{"name":"myredis", "region":"global", "primary_region":"us-east-1", "read_regions":["us-west-1","us-west-2"], "tls": true}'
```
