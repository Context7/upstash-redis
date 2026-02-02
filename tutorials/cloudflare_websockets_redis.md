Skip to content
You signed in with another tab or window. Reload to refresh your session. You signed out in another tab or window. Reload to refresh your session. You switched accounts on another tab or window. Reload to refresh your session. Dismiss alert
{{ message }}
upstash  / **examples ** Public
  * Notifications  You must be signed in to change notification settings
  * Fork 18
  * Star  40


## Collapse file tree
## Files
main
Search this repository
/
# cloudflare-websockets
/
Copy path
## Directory actions
## More options
More options
## Directory actions
## More options
More options
## Latest commit
fahreddinozcan
convert worker from submodule to regular directory
failure
Jan 6, 2025
db39461 · Jan 6, 2025
## History
History
Open commit details
History
/
# cloudflare-websockets
/
Top
## Folders and files
Name| Name| Last commit message| Last commit date  
---|---|---|---  
### parent directory
..  
client| client| add: cloudflare websockets example| Jan 6, 2025  
worker| worker| convert worker from submodule to regular directory| Jan 6, 2025  
README.md| README.md| add: cloudflare websockets example| Jan 6, 2025  
View all files  
## README.md
Outline
title | products | languages | stack | platforms | use_cases | author | preview_url  
---|---|---|---|---|---|---|---  
Serverless WebSocket Chat on CF Workers |  | redis  
---  
| ts  
---  
| React | WebSocket  
---|---  
| Cloudflare  
---  
| State Store  
---  
fahreddinozcan | https://486e5d1a.client-260.pages.dev  
  

### Real-time WebSocket Chat
Build a real-time chat application using Cloudflare Workers, WebSocket API, and Upstash Redis 
This example demonstrates how to create a serverless real-time chat application using Cloudflare Workers WebSocket API for real-time communication and Upstash Redis for message persistence. The frontend is built with React and deployed on Cloudflare Pages.
You can see the demo here
# Project Details
The goal of this project is to create a serverless chat application without maintaining any traditional WebSocket servers. To achieve this, we use Cloudflare Workers with its WebSocket API for handling real-time connections, and Upstash Redis sorted sets for message persistence. The frontend is a React application that connects to the Worker via WebSocket.
## Real-time Communication with WebSocket
The application uses Cloudflare Workers' WebSocket API to handle real-time bidirectional communication. Each client maintains a WebSocket connection to the Worker, which handles message broadcasting and persistence. The system includes:
  * Real-time message delivery
  * Automatic reconnection handling
  * Connection status indicators
  * Message history on connection


## Message Storage with Redis
We use Upstash Redis sorted sets to store chat messages with timestamps as scores. This provides:
  * Efficient message storage and retrieval
  * Automatic message ordering by timestamp
  * Easy pagination for message history
  * Message persistence across connections


## Features
  * Real-time bidirectional communication
  * Message persistence with Redis sorted sets
  * Automatic reconnection handling
  * Connection status indicators
  * Message history on connection
  * Clean mobile-responsive UI
  * Modern chat bubble interface
  * Typing indicators (optional)


# Deployment
## Prerequisites
  1. Upstash Redis database
  2. Cloudflare account
  3. wrangler CLI installed (`npm i -g wrangler`)


## Environment Variables
Edit the environment variables in the `wrangler.toml` file of your `worker` directory:
```
name = "chat-app"
main = "src/index.ts"
compatibility_date = "2024-01-01"

[vars]
UPSTASH_REDIS_REST_URL = "YOUR_REDIS_URL"
UPSTASH_REDIS_REST_TOKEN = "YOUR_REDIS_TOKEN"
```

## Deploy the Worker
```
cd worker
pnpm install
npm run deploy
```

## Deploy the Frontend
```
cd client
pnpm install
pnpm run deploy
```

### Learn More
To learn more about the technologies used, check out:
  * Upstash Redis Documentation
  * Cloudflare Workers Documentation
  * Cloudflare WebSocket API
  * Upstash Discord


You can’t perform that action at this time. 
