# mcp-installer - A MCP Server to install MCP Servers

This server is a server that installs other MCP servers for you. Install it, and you can ask your AI to install MCP servers hosted in npm or PyPi for you. Requires `npx` and `uv` to be installed for node and Python servers respectively.


![image](https://github.com/user-attachments/assets/d082e614-b4bc-485c-a7c5-f80680348793)

### How to install:

Put this into your `claude_desktop_config.json` (either at `~/Library/Application Support/Claude` on macOS or `C:\Users\NAME\AppData\Roaming\Claude` on Windows):


```json
{
  "mcpServers": {
    "mcp-installer": {
      "command": "npx",
      "args": [
        "@anibetts/mcp-installer"
      ],
    }
  }
}
```
or to your custom  `config.json` file if you are using one. This allow you to install MCP servers using the `mcp-installer` server. in any MCP client.
```json
  "mcpServers": {
    "mcp-installer": {
      "command": "npx",
      "args": [
        "@thiago4go/mcp-installer",
        "--recursive"
      ],
      "env": {
        "MCP_DESKTOP_CONFIG": "path/to/your/mcp_client_config.json"
      },
    }
  }
```

### Example prompts

> Hey Chat, install the MCP server named mcp-server-fetch

> Hey Chat, install the @modelcontextprotocol/server-filesystem package as an MCP server. Use ['/Users/anibetts/Desktop'] for the arguments

> Hi Chat, please install the MCP server at /Users/anibetts/code/mcp-youtube, I'm too lazy to do it myself.

> Install the server @modelcontextprotocol/server-github. Set the environment variable GITHUB_PERSONAL_ACCESS_TOKEN to '1234567890'
