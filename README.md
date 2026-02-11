# FURNACE Releases

Extension distributions and install instructions for [FURNACE](https://github.com/forgewithfurnace/) -- the AI-powered MCP server for structured code generation, analysis, and project orchestration.

## IDE Extensions

### VS Code -- "Forge with Furnace"

Download the `.vsix` file from this repo and install manually:

```bash
code --install-extension extensions/vscode/furnace-forge-project-0.4.1.vsix
```

Or search **"Forge with Furnace"** on the VS Code Marketplace.

### JetBrains -- "furnace-project"

Download the `.zip` file from this repo and install via:

**Settings > Plugins > Gear icon > Install Plugin from Disk** -- select the `.zip` file.

Or search **"furnace-project"** on the JetBrains Marketplace (IntelliJ, WebStorm, PyCharm, GoLand, CLion, etc.).

## Pre-built Binaries

Pre-built binaries are hosted on [GitHub Releases](https://github.com/forgewithfurnace/furnace-releases/releases).

| Platform | Notes |
|----------|-------|
| macOS (Apple Silicon) | Also runs on Intel Macs via Rosetta 2 |
| Linux (x86_64) | |
| Windows (x86_64) | |

### Install via npm (recommended)

```bash
npm install -g furnace-mcp
```

### MCP client config

```json
{"mcpServers": {"furnace": {"command": "npx", "args": ["-y", "furnace-mcp"]}}}
```

### Install from binary

```bash
# macOS (Apple Silicon — also runs on Intel via Rosetta 2)
curl -L https://github.com/forgewithfurnace/furnace-releases/releases/latest/download/furnace-aarch64-apple-darwin.tar.gz | tar xz
sudo mv furnace /usr/local/bin/

# Linux (x86_64)
curl -L https://github.com/forgewithfurnace/furnace-releases/releases/latest/download/furnace-x86_64-unknown-linux-gnu.tar.gz | tar xz
sudo mv furnace /usr/local/bin/

# Windows (x86_64) — download the .zip from GitHub Releases, extract, add furnace.exe to PATH
```

### From crates.io

```bash
cargo install furnace-mcp
```

## Current Version

| Component | Version |
|-----------|---------|
| FURNACE MCP Server | 0.4.1 |
| VS Code Extension | 0.4.1 |
| IntelliJ Plugin | 0.4.1 |

## What is FURNACE?

FURNACE (Formal Unified Runtime for Network-Augmented Code Engineering) is a Rust MCP server that sits between your LLM and your codebase. It provides:

- **27 MCP tools** for code search, generation, validation, and automated workflows
- **9 AI agents** -- Gandalf, Gimli, Trinity, Legolas, Morpheus, Elrond, Aragorn, AutoForge, SearchOrchestrator
- **Tiered search** -- vector (Tier 1), hybrid (Tier 2), agentic (Tier 3)
- **3 embedded databases** -- SQLite, KuzuDB (graph), LanceDB (vectors)
- **Zero external services** -- single binary, no Docker, no cloud dependencies
- **External KB sync** -- ChromaDB, Pinecone, Weaviate integration
- **Bidirectional sync** -- Linear, Jira, Notion
- **IDE extensions** -- VS Code and JetBrains with live dashboards, SCROLL editors, and visual search

Learn more at [github.com/forgewithfurnace/furnace](https://github.com/forgewithfurnace/).
