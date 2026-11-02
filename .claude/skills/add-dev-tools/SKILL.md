---
name: add-dev-tools
description: Use after the tech is chosen, whenever it changes, or when you need current docs. Finds and adds official docs, skills and MCP servers for this project.
---

# Add docs and tools

For each part of the stack, such as React, Vite or Firebase, look in this order:

1. An official Claude Code plugin or skills from the vendor
2. An official docs MCP server from the vendor
3. An official docs site, or its `llms.txt`

**Use vendor-published sources only.** Skip third-party plugins and servers unless the user asks, since this project runs with few permission prompts. If you think one is worth it, explain why and ask, as a risk to their computer.

## How to add them

- **Plugin:** run `claude plugin install <name>@<marketplace> --scope project`, adding the marketplace first if needed. The `claude` command is often missing from the path in the desktop app, so if it fails, give the user the steps with `human-step`: the **+** button next to the prompt box, then **Add plugins**.
- **MCP server:** add it to `.mcp.json` in this folder. On Windows, use `cmd /c` to run `npx`. It takes effect in a new session and may ask for approval once, so tell the user.
- **Docs only:** write the links in `memory/tooling.md`, and read them when you need them.

Don't stop work because a tool won't install. Official docs through web fetch are enough to continue. Tell the user only if they need to do something.

## Firebase

Firebase publishes an official Claude Code plugin with skills and an MCP server. See https://firebase.google.com/docs/ai-assistance/build-with-ai for current commands. Without the `claude` command, this `.mcp.json` entry gives you the MCP server:

```json
{
  "mcpServers": {
    "firebase": {
      "command": "cmd",
      "args": ["/c", "npx", "-y", "firebase-tools@latest", "mcp"]
    }
  }
}
```

Record what you added and its source in `memory/tooling.md`, then commit.
