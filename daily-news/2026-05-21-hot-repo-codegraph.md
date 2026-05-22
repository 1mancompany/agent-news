---
title: "🔥 Hot Repo: Pre-Index Your Codebase, Cut Claude Code Costs 35%"
author: OMC Editorial
published_at: 2026-05-21T13:13:40.852288+00:00
slug: hot-repo-codegraph
image: https://github.com/user-attachments/assets/f168182f-4d9a-44e0-94d7-08d018cc8a3a
source: https://news.one-man-company.com/news/hot-repo-codegraph
---

> **One-liner** — CodeGraph is a local MCP server that pre-indexes your codebase into a SQLite knowledge graph, so AI coding agents like Claude Code and Cursor can answer architecture questions without scanning files.

- **Repo:** [colbymchenry/codegraph](https://github.com/colbymchenry/codegraph)
- **Stars:** ⭐ 12,058 (+2,123 today)
- **Language:** TypeScript
- **License:** MIT

---

## What It Does

CodeGraph builds a pre-indexed knowledge graph of your codebase — symbols, call graphs, routing patterns, and file relationships — stored locally in SQLite with FTS5 full-text search. It exposes this as an MCP server, so agents like Claude Code, Cursor, Codex CLI, and OpenCode can answer architecture questions by querying the graph directly instead of spawning Explore sub-agents that grep and read files.

## Why It's Blowing Up

v0.8.0 shipped May 20 alongside benchmarks that are hard to ignore: tested across 7 real-world codebases in 7 languages using Claude Opus 4.7 headlessly, the results averaged **35% cheaper, 59% fewer tokens, 49% faster, and 70% fewer tool calls** compared to agents without the index. On large repos like VS Code (~10k files), the savings hit 72% fewer tool calls and 73% fewer tokens.

The release also fixed two high-impact bugs: WSL2 users on NTFS `/mnt/*` mounts had the MCP server hang on startup because the file watcher was crossing the Windows/9p boundary; and project-local Claude Code installs were silently writing to `.claude.json` instead of `.mcp.json` — meaning the codegraph tools never appeared. Both fixes unblocked a large chunk of users who had given up.

The timing aligns with a broader developer conversation: as Claude Code usage grows on larger codebases, exploration agent costs have become the dominant line item on API bills. CodeGraph's approach — a pre-built, always-fresh index served over MCP — is a clean architectural answer.

## Key Features

- **Code knowledge graph** — Tree-sitter-parsed symbols, call edges, and file relationships stored in SQLite FTS5
- **Framework-aware routing** — Recognizes URL patterns across Django, FastAPI, Express, NestJS, Rails, Spring, and 7 more frameworks
- **Always-fresh index** — Native OS file events (FSEvents/inotify/ReadDirectoryChangesW) with debounced incremental sync; WSL2 falls back to git-hook sync
- **19+ languages** — TypeScript, Python, Go, Rust, Java, C#, Swift, Kotlin, Dart, and more
- **100% local** — No API keys, no cloud uploads, no telemetry; everything lives in `.codegraph/`

## Quick Start

```bash
npx @colbymchenry/codegraph    # interactive installer, auto-detects Claude Code / Cursor / Codex / OpenCode
cd your-project
codegraph init -i              # builds the local knowledge graph index
```

## The Verdict

If you run Claude Code on repos with more than ~500 files, CodeGraph is almost certainly worth the install — the cost reductions are benchmarked and scale with repo size. On a tiny project under ~100 files the gains narrow, since native grep is already cheap. WSL2 users on NTFS mounts can now use it safely with v0.8.0. Run `npx @colbymchenry/codegraph`, let it auto-configure your agent, and check your API bill after a week.

📎 [GitHub](https://github.com/colbymchenry/codegraph) · [npm](https://www.npmjs.com/package/@colbymchenry/codegraph) · [Author's writeup](https://medium.com/@me_82386/i-cut-my-claude-code-api-costs-by-40-with-one-tool-12cf4306a1ab)