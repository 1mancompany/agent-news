---
title: "🔥 Hot Repo: 120x Token Savings, Zero Runtime Dependencies"
author: OMC Editorial
published_at: 2026-06-17T13:10:19.488112+00:00
slug: hot-repo-codebase-memory-mcp
image: https://raw.githubusercontent.com/DeusData/codebase-memory-mcp/main/docs/graph-ui-screenshot.png
source: https://news.one-man-company.com/news/hot-repo-codebase-memory-mcp
---

> **One-liner** — codebase-memory-mcp is a zero-dependency MCP server that maps any codebase into a persistent knowledge graph, slashing LLM token usage by up to 120x compared to file-by-file code exploration.

- **Repo:** [DeusData/codebase-memory-mcp](https://github.com/DeusData/codebase-memory-mcp)
- **Stars:** ⭐ 4,273 (+367 today)
- **Language:** C
- **License:** MIT

---

## What It Does

codebase-memory-mcp is an MCP server written in pure C that parses your entire codebase using tree-sitter AST analysis, storing functions, classes, call chains, and HTTP routes in a persistent SQLite knowledge graph. Instead of an AI agent reading dozens of files to answer "where is this function called?", it runs a sub-millisecond graph query. The result: 5 structural queries cost ~3,400 tokens versus ~412,000 tokens via traditional file-by-file search — a 120x reduction.

## Why It's Blowing Up

A preprint on arXiv (2603.27277) dropped alongside the v0.8.1 release and validated the approach across 31 real-world repositories: 83% answer quality, 10x fewer tokens, and 2.1x fewer tool calls versus standard file exploration. Developers working with Claude Code and Codex have been hunting for exactly this kind of structural shortcut as context windows fill up and per-token costs compound.

The tool also hit a tipping point in breadth: the `install` command now auto-detects and configures 11 coding agents simultaneously — Claude Code, Codex CLI, Gemini CLI, Zed, OpenCode, Aider, KiloCode, VS Code, OpenClaw, Antigravity, and Kiro. One command, all agents wired up. That kind of zero-friction story spreads fast in developer communities.

A secondary driver is the delivery format: a single static C binary with zero runtime dependencies. No Node.js, no Python, no Docker. That eliminates the biggest friction point in MCP adoption — the setup tax that kills adoption before you even try a tool.

## Key Features

- **158-language support** — all grammars compiled into the binary via vendored tree-sitter; nothing extra to install
- **Hybrid LSP** — semantic type resolution for Python, TypeScript, Go, C/C++, Java, Rust, and five more languages
- **14 MCP tools** — search, call-graph tracing, dead code detection, impact analysis, Cypher queries, and ADR management
- **3D graph visualization** — optional built-in UI at localhost:9749 to explore the knowledge graph interactively
- **Infrastructure-as-code indexing** — Dockerfiles, Kubernetes manifests, and Kustomize overlays indexed as graph nodes with cross-references

## Quick Start

```bash
curl -fsSL https://raw.githubusercontent.com/DeusData/codebase-memory-mcp/main/install.sh | bash
```

Restart your coding agent, then say **"Index this project"**. Done.

## The Verdict

If you use Claude Code, Codex CLI, or any of the 11 supported agents on a non-trivial codebase, this is an immediate quality-of-life upgrade — less context stuffed with raw file contents, faster answers on structural questions, and meaningfully lower token costs. The zero-dependency C binary means it installs cleanly and doesn't rot when Node or Python versions change. Skip it if your codebase is under a few thousand lines; file reads are fine at that scale. Everyone else: star it and run the installer.

📎 [GitHub](https://github.com/DeusData/codebase-memory-mcp) · [Homepage](https://deusdata.github.io/codebase-memory-mcp/) · [arXiv Paper](https://arxiv.org/abs/2603.27277)
