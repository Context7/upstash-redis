> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Upstash MCP

We provide an open source Upstash MCP to use natural language to interact with your Upstash account, e.g.:

* "Create a new Redis database in us-east-1"
* "List my databases"
* "Show all keys starting with "user:" in my users-db"
* "Create a backup"
* "Show me the throughput spikes for the last 7 days"

***

## Quickstart

### Step 1: Get your API Key

1. Go to `Account > Management API > Create API key` and create an API key.
   <img src="https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/mcp/create-upstash-api-key.png?fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=6f836a85ae3c72966f48885c3d450831" data-og-width="1920" width="1920" data-og-height="1080" height="1080" data-path="img/mcp/create-upstash-api-key.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/mcp/create-upstash-api-key.png?w=280&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=a6a4f5b04f9ddaf4c95b8a2c541093bd 280w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/mcp/create-upstash-api-key.png?w=560&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=5e82b612cffa5b4224be9ba12bd25798 560w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/mcp/create-upstash-api-key.png?w=840&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=409adc475e28bdbc45b1a357531bb08a 840w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/mcp/create-upstash-api-key.png?w=1100&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=47cdc98dfc7f4c47128dcdc29e30cd51 1100w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/mcp/create-upstash-api-key.png?w=1650&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=30e541dfa7bd93358c5fe48b0de53451 1650w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/mcp/create-upstash-api-key.png?w=2500&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=b2d6163be507df6c7a430d143c6f4a7d 2500w" />
2. Note down your `<UPSTASH_EMAIL>` and `<UPSTASH_API_KEY>`.

***

### Step 2: Locate `mcp.json`

* **Cursor**: Navigate to `Cursor Settings > Features > MCP` and click `+ Add new global MCP server`. This will open the `mcp.json` file.
  <img src="https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/mcp/cursor-mcp-settings.png?fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=397c0ef714c08e365b83721b1e383f2f" data-og-width="1919" width="1919" data-og-height="1080" height="1080" data-path="img/mcp/cursor-mcp-settings.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/mcp/cursor-mcp-settings.png?w=280&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=2e42d06225b9b189b9be686e72752c05 280w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/mcp/cursor-mcp-settings.png?w=560&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=a8e5939c5760be8edbab1cedf2770f09 560w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/mcp/cursor-mcp-settings.png?w=840&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=068b5ddc6f021a55158ca03bc913d357 840w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/mcp/cursor-mcp-settings.png?w=1100&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=c138d351742e6cb2ac3607d70b1c6320 1100w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/mcp/cursor-mcp-settings.png?w=1650&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=3c00c5fcb0c671d727b36084b2200490 1650w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/mcp/cursor-mcp-settings.png?w=2500&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=197f47de70b9ee3336962b0758178606 2500w" />
* **Claude**: Navigate to `Settings > Developer` and click `Edit Config`. This will open the `claude_desktop_config.json` file. [Refer to the MCP documentation for more details](https://modelcontextprotocol.io/quickstart/user).
* **Copilot**: Create a `.vscode/mcp.json` file in your workspace directory. For Copilot, first update the `mcp.json` file as described in the next step on this page, then follow the [Copilot documentation (starting from step 2)](https://docs.github.com/en/copilot/customizing-copilot/extending-copilot-chat-with-mcp#configuring-mcp-servers-in-visual-studio-code) to configure MCP servers in VS Code Chat.

***

### Step 3: Configure the MCP Server

#### Claude Code CLI (Recommended with Claude)

If you're using Claude Code, the easiest way to add the Upstash MCP server is via the CLI:

```bash  theme={"system"}
claude mcp add upstash -- npx -y @upstash/mcp-server@latest \
  --email <UPSTASH_EMAIL> \
  --api-key <UPSTASH_API_KEY>
```

Verify the installation:

```bash  theme={"system"}
claude mcp list
```

To share with your team (adds to `.mcp.json` in your project):

```bash  theme={"system"}
claude mcp add upstash --scope project -- npx -y @upstash/mcp-server@latest \
  --email <UPSTASH_EMAIL> \
  --api-key <UPSTASH_API_KEY>
```

#### JSON Configuration (Cursor, Claude Desktop, Copilot)

Add the following configuration to your MCP file:

<CodeGroup>
  ```json Cursor & Claude Desktop theme={"system"}
  {
    "mcpServers": {
      "upstash": {
        "command": "npx",
        "args": [
          "-y",
          "@upstash/mcp-server@latest",
          "--email",
          "<UPSTASH_EMAIL>",
          "--api-key",
          "<UPSTASH_API_KEY>"
        ]
      }
    }
  }
  ```

  ```json Copilot theme={"system"}
  {
    "servers": {
      "upstash": {
        "type": "stdio",
        "command": "npx",
        "args": [
          "-y",
          "@upstash/mcp-server@latest",
          "--email",
          "<UPSTASH_EMAIL>",
          "--api-key",
          "<UPSTASH_API_KEY>"
        ]
      }
    }
  }
  ```
</CodeGroup>

***

### Step 4: Use MCP with Your Client

Once your MCP is configured, your client can now interact with the MCP server for tasks like:

* Seeding data
* Querying databases
* Creating new databases
* Managing backups
* Analyzing performance metrics

For example, you can ask your client to "add ten users to my Redis database" or "show me the throughput spikes for the last 7 days."
