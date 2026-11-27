<img src=".claude-plugin/icon.png" width="72" alt="GT Protocol">

# GT Protocol for Claude, Claude Code, ChatGPT and Codex — apps and terminal

Connects GT App (GT Protocol) to Claude, Claude Code, ChatGPT and Codex, in their apps and in the terminal, to analyze the market and test strategies: market data, GT's signals, backtests and demo (paper) bots. Ask in plain words to check the market, backtest a strategy, or try it on a demo bot.

This repository holds no code. It adds one remote MCP server, `https://mcp.gt-protocol.io/mcp`, run by GT Protocol. You sign in to GT App and click Allow, and the AI app then calls GT App on your behalf.

## Claude chat (claude.ai or the Chat tab in the Claude app)

1. In the left menu, open Customize (Plugins) → Connectors
2. Click + Add → Add custom connector
3. Name: GT Protocol, URL: `https://mcp.gt-protocol.io/mcp` → Continue
4. Keep the detected sign-in settings → Continue → Sign in now → Add
5. GT App opens: sign in and click Allow
6. In a chat, click + at the bottom left → Connectors and make sure GT Protocol is turned on

## Claude Code in the Claude app (Code tab)

1. Click your profile at the bottom left → Settings
2. Open Customize (Plugins) → Connectors
3. Scroll down → Browse plugins → Connectors
4. Click + Add → Add custom connector
5. Name: GT Protocol, URL: `https://mcp.gt-protocol.io/mcp` → Continue
6. Keep the detected sign-in settings → Continue → Sign in now → Add
7. GT App opens: sign in and click Allow

## Claude Code in the terminal

1. Run: `claude plugin install gt-protocol --marketplace iconic-tm/mcp_plugin`
2. Start a new session with `claude` and type /mcp → plugin:gt-protocol:gt-protocol → Authenticate
3. GT App opens: sign in and click Allow

Inside a session, `/plugin install gt-protocol --marketplace iconic-tm/mcp_plugin` does the same. This needs Claude Code 2.1.292 or later; on an older version, run `claude mcp add --transport http --scope user gt-protocol https://mcp.gt-protocol.io/mcp` instead (then /mcp → gt-protocol → Authenticate). Use one way, not both, or the tools appear twice.

## ChatGPT

1. Open Plugins (or go to chatgpt.com/plugins)
2. Click + → Add custom MCP server
3. Name: GT Protocol, Connection: Server URL, URL: `https://mcp.gt-protocol.io/mcp`
4. Set Authentication to OAuth and keep the supported OAuth discovery settings
5. Check "I understand and want to continue" → Create as a plugin
6. Review the detected GT Protocol tools
7. Open the new plugin under Plugins → Personal and click + to install it
8. When GT App opens: sign in and click Allow
9. Back in ChatGPT, switch from Chat to Work and start a new task
10. Type @ and choose GT Protocol

## Codex desktop app

1. Open Settings → MCP servers
2. Click Add server
3. Name: GT Protocol, type: Streamable HTTP, URL: `https://mcp.gt-protocol.io/mcp`
4. Click Save → Restart
5. Go back to MCP servers → GT Protocol → Authenticate (if asked)
6. GT App opens: sign in and click Allow
7. Open a new session and check that GT Protocol is available

## Codex in the terminal

1. Run: `codex plugin marketplace add iconic-tm/mcp_plugin`
2. Run: `codex plugin add gt-protocol@gt-protocol`
3. Run: `codex mcp login gt-protocol`. GT App opens: sign in and click Allow
4. Start a new session with `codex` and type /mcp to check the connection

## Trading

Demo (paper) is the default. Before a live bot or trade, the AI shows you its settings and places it only after you confirm. Backtests include fees and slippage; a past result is not a forecast.

## Support

- Contact: https://www.gt-protocol.io/contacts/
- Privacy policy: https://www.gt-protocol.io/privacy-policy/
- Terms of service: https://www.gt-protocol.io/terms-of-service/
