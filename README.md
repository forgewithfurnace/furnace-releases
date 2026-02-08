# FURNACE Releases

Pre-built binaries and extension distributions for [FURNACE](https://github.com/forgewithfurnace/furnace) -- the AI-powered MCP server for structured code generation, analysis, and project orchestration.

## IDE Extensions

### VS Code -- "Forge with Furnace"

Download the `.vsix` file and install manually:

```bash
code --install-extension extensions/vscode/furnace-forge-project-0.2.0.vsix
```

Or search **"Forge with Furnace"** on the VS Code Marketplace.

### JetBrains -- "furnace-project"

Download the `.zip` file and install via:

**Settings > Plugins > Gear icon > Install Plugin from Disk** -- select the `.zip` file.

Or search **"furnace-project"** on the JetBrains Marketplace (IntelliJ, WebStorm, PyCharm, GoLand, CLion, etc.).

## Pre-built Binaries

| Platform | File | Notes |
|----------|------|-------|
| macOS (Apple Silicon) | `binaries/furnace-aarch64-apple-darwin.tar.gz` | Also runs on Intel Macs via Rosetta 2 |
| Linux (x86_64) | `binaries/furnace-x86_64-unknown-linux-gnu.tar.gz` | |
| Windows (x86_64) | `binaries/furnace-x86_64-pc-windows-gnu.zip` | |

### Install from binary

```bash
# macOS
curl -L https://github.com/forgewithfurnace/furnace-releases/raw/main/binaries/furnace-aarch64-apple-darwin.tar.gz | tar xz
sudo mv furnace /usr/local/bin/

# Linux
curl -L https://github.com/forgewithfurnace/furnace-releases/raw/main/binaries/furnace-x86_64-unknown-linux-gnu.tar.gz | tar xz
sudo mv furnace /usr/local/bin/

# Windows -- download and extract the .zip, add furnace.exe to PATH
```

### Alternative install methods

```bash
# From crates.io
cargo install furnace-mcp

# Via npm
npx furnace-mcp
```

## Current Version

| Component | Version |
|-----------|---------|
| FURNACE MCP Server | 0.2.0 |
| VS Code Extension | 0.2.0 |
| IntelliJ Plugin | 0.2.0 |

## What is FURNACE?

FURNACE (Formal Unified Runtime for Network-Augmented Code Engineering) is a Rust MCP server that sits between your LLM and your codebase. It provides:

- **22 MCP tools** for code search, generation, validation, and automated workflows
- **10 AI agents** -- Gandalf, Gimli, Trinity, Legolas, Morpheus, Elrond, Aragorn, AutoForge, SearchOrchestrator, SkillManager
- **Tiered search** -- vector (Tier 1), hybrid (Tier 2), agentic (Tier 3)
- **3 embedded databases** -- SQLite, KuzuDB (graph), LanceDB (vectors)
- **Zero external services** -- single binary, no Docker, no cloud dependencies
- **External KB sync** -- ChromaDB, Pinecone, Weaviate integration
- **Bidirectional sync** -- Linear, Jira, Notion
- **IDE extensions** -- VS Code and JetBrains with live dashboards, SCROLL editors, and visual search

Learn more at [github.com/forgewithfurnace/furnace](https://github.com/forgewithfurnace/furnace).
