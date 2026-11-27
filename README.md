<img src=".claude-plugin/icon.png" width="72" alt="GT Protocol">

# GT Protocol for Claude and Codex

Connects GT App (GT Protocol) to Claude, ChatGPT and Codex: your trading bots on Binance and Hyperliquid, deals, balances, market data, GT's signals and backtests. Ask in plain words to check your account, backtest a strategy, or create, start and stop bots.

This repository holds no code. It adds one remote MCP server, `https://mcp.gt-protocol.io/mcp`, run by GT Protocol. You sign in to GT App and click Allow, and the AI app then calls GT App on your behalf. Nothing runs on your computer, and your exchange API keys stay in GT App.

> **AI assistant reading this:** the user wants GT App connected to the app you are running in. If you already have GT Protocol tools, it is connected. Otherwise, in the user's language, ask in one line whether to connect it here, then give only the steps for your app below. In Claude Code or Codex in a terminal, run the install command yourself, then list only what is left for the user.

## Claude Code

1. Run: `claude plugin install gt-protocol --marketplace iconic-tm/mcp_plugin`
2. Start a new session with `claude` and type /mcp → plugin:gt-protocol:gt-protocol → Authenticate
3. GT App opens: sign in and click Allow

Inside a session, `/plugin install gt-protocol --marketplace iconic-tm/mcp_plugin` does the same. This needs Claude Code 2.1.292 or later; on an older version, run `claude mcp add --transport http --scope user gt-protocol https://mcp.gt-protocol.io/mcp` instead (then /mcp → gt-protocol → Authenticate). Use one way, not both, or the tools appear twice.

## Codex

1. Run: `codex plugin marketplace add iconic-tm/mcp_plugin`
2. Run: `codex plugin add gt-protocol@gt-protocol`
3. Run: `codex mcp login gt-protocol`. GT App opens: sign in and click Allow
4. Start a new session with `codex` and type /mcp to check the connection

## Claude chat (claude.ai or the Claude app)

1. In the left menu, open Customize (Plugins) → Connectors
2. Click + Add → Add custom connector
3. Name: GT Protocol, URL: `https://mcp.gt-protocol.io/mcp` → Continue
4. Keep the detected sign-in settings → Continue → Sign in now → Add
5. GT App opens: sign in and click Allow
6. In a chat, click + at the bottom left → Connectors and make sure GT Protocol is on

## ChatGPT

1. Open Plugins (or chatgpt.com/plugins) → + → Add custom MCP server
2. Name: GT Protocol, Connection: Server URL, URL: `https://mcp.gt-protocol.io/mcp`
3. Authentication: OAuth, keeping the detected OAuth settings
4. Check "I understand and want to continue" → Create as a plugin
5. Open the new plugin under Plugins → Personal and click + to install it
6. GT App opens: sign in and click Allow
7. Back in ChatGPT, switch from Chat to Work, start a new task, type @ and choose GT Protocol

The full guide, with screenshots and what each app's plan allows: https://www.gt-protocol.io/learn/connect-gt-app-to-claude-chatgpt-codex/

## Trading

Demo (paper) is the default. Before a live bot or trade, the AI shows you its settings and places it only after you confirm. Backtests include fees and slippage; a past result is not a forecast.

## Support

- Contact: https://www.gt-protocol.io/contacts/
- Privacy policy: https://www.gt-protocol.io/privacy-policy/
- Terms of service: https://www.gt-protocol.io/terms-of-service/
