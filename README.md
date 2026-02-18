# Phantom Connect SDK — Cursor Plugin

AI-powered assistance for integrating the Phantom Connect SDK into your Solana and EVM applications. This Cursor plugin provides skills, rules, an agent, and a live MCP server so Cursor can scaffold projects, write correct integration code, and search Phantom docs in real-time.

## Installation

1. Clone or copy this plugin into your Cursor plugins directory, or open the folder in Cursor.
2. Cursor will automatically detect the `.cursor-plugin/plugin.json` manifest.
3. The MCP server (`phantom-docs`) will appear in your MCP settings — verify it connects to `https://docs.phantom.com/mcp`.

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

### Rules (Always Active)

| Rule | What It Enforces |
|------|------------------|
| **phantom-sdk-best-practices** | Use `signAndSendTransaction`, proper provider setup, error handling, connection checks |
| **solana-transaction-safety** | Use `LAMPORTS_PER_SOL`, verify transactions, correct network selection, no key exposure |
| **embedded-wallet-constraints** | No `signTransaction`, spending limits, session duration, polyfill requirements |

### Agent

**Phantom Integration Specialist** — A specialist agent that knows all three SDKs, can scaffold projects, validates code against constraints, and uses the Phantom docs MCP server for up-to-date information.

### MCP Server

**phantom-docs** — Connects to Phantom's official documentation server at `https://docs.phantom.com/mcp` for real-time API reference and examples.

## Usage

Once installed, ask the Cursor agent to:

- "Set up a React app with Phantom Connect"
- "Add social login with Google and Apple"
- "Send 0.1 SOL to an address"
- "Implement Sign-in with Solana"
- "Set up a React Native app with Phantom wallet"

The agent will follow the plugin's skills and rules to generate correct, safe integration code.

## Requirements

- [Cursor](https://cursor.sh) editor
- A Phantom Portal account for `appId` registration: [portal.phantom.com](https://portal.phantom.com)

## License

MIT
