# Phantom Connect — Cursor Plugin

Give your agent a wallet. Swap, sign, and manage addresses across Phantom's supported chains — and tap into Phantom's docs for context. This plugin also includes skills, rules, and agents to help scaffold wallet-connected apps with the Phantom Connect SDK across React, React Native, and vanilla JS/TS.

## Installation

1. Clone or copy this plugin into your Cursor plugins directory, or open the folder in Cursor.
2. Cursor will automatically detect the `.cursor-plugin/plugin.json` manifest.
3. The MCP servers (`phantom-connect-sdk` and `phantom-mcp`) will appear in your MCP settings.

## What's Included

### Skills

| Skill | Description |
|-------|-------------|
| **setup-react-app** | Scaffold a React app with `@phantom/react-sdk`, PhantomProvider, ConnectButton, and hooks |
| **setup-browser-app** | Scaffold a vanilla JS/TS app with `@phantom/browser-sdk` singleton pattern |
| **setup-react-native-app** | Scaffold a React Native (Expo) app with `@phantom/react-native-sdk` and required polyfills |
| **send-sol-transaction** | Build and send SOL transfers with proper signing and verification |
| **sign-message** | Implement message signing for Solana and EVM, including SIWS authentication |
| **add-social-login** | Configure Google/Apple social login with embedded wallet support |
| **phantom-wallet-mcp** | Execute wallet operations via the Phantom MCP — addresses, transfers, signing, swaps |

### Rules (Always Active)

| Rule | What It Enforces |
|------|------------------|
| **phantom-sdk-best-practices** | Use `signAndSendTransaction`, proper provider setup, error handling, connection checks |
| **solana-transaction-safety** | Use `LAMPORTS_PER_SOL`, verify transactions, correct network selection, no key exposure |
| **embedded-wallet-constraints** | No `signTransaction`, spending limits, session duration, polyfill requirements |

### Agents

| Agent | Purpose |
|-------|---------|
| **Phantom Integration Specialist** | SDK integration — scaffolds projects, writes correct code, validates against constraints, and looks up Phantom docs in real-time |
| **Phantom Wallet Agent** | Wallet operations — get addresses, transfer tokens, sign transactions, execute swaps, and sign messages via the `phantom-mcp` server |

### MCP Servers

| Server | Transport | Description |
|--------|-----------|-------------|
| **phantom-connect-sdk** | SSE | Phantom Connect SDK documentation at `https://docs.phantom.com/mcp` for real-time API reference |
| **phantom-mcp** | stdio | Wallet operations via [`@phantom/mcp-server`](https://www.npmjs.com/package/@phantom/mcp-server) — sign transactions, transfer tokens, buy tokens, sign messages |

The `phantom-mcp` server requires a `PHANTOM_APP_ID` environment variable from [Phantom Portal](https://portal.phantom.com). Set it in your environment or Cursor MCP settings.

## Usage

Once installed, ask the Cursor agent to:

- "Set up a React app with Phantom Connect"
- "Add social login with Google and Apple"
- "Send 0.1 SOL to an address"
- "Implement Sign-in with Solana"
- "Set up a React Native app with Phantom wallet"
- "Get my wallet addresses"
- "Transfer 0.5 SOL to [address]"
- "Sign this message with my wallet"

The agent will follow the plugin's skills and rules to generate correct, safe integration code.

## Requirements

- [Cursor](https://cursor.sh) editor
- A Phantom Portal account for `appId` registration: [portal.phantom.com](https://portal.phantom.com)

## License

MIT
