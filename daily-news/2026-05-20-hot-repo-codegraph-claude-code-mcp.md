---
title: "🔥 Hot Repo: 94% Fewer Calls — Claude Code’s Missing Piece"
author: OMC Editorial
published_at: 2026-05-20T13:09:00.759193+00:00
slug: hot-repo-codegraph-claude-code-mcp
image: https://opengraph.githubassets.com/1/colbymchenry/codegraph
source: https://news.one-man-company.com/news/hot-repo-codegraph-claude-code-mcp
---

> **One-liner** — CodeGraph is a local-first MCP server that pre-indexes your codebase into a SQLite knowledge graph, letting Claude Code, Cursor, and Codex explore symbols and call graphs with 92% fewer tool calls.

- **Repo:** [colbymchenry/codegraph](https://github.com/colbymchenry/codegraph)
- **Stars:** ⭐ 7,800 (+~200 today)
- **Language:** TypeScript
- **License:** MIT

---

## What It Does

CodeGraph parses your codebase with tree-sitter, stores symbols, relationships, and call graphs in a local SQLite database, and exposes that knowledge to AI agents over MCP. Instead of agents blasting grep commands and reading dozens of files to understand a codebase, they issue a single `codegraph_explore` call and get rich, structured context back instantly. The tool watches for file changes using native OS events and reindexes automatically.

## Why It's Blowing Up

The frustration is familiar to anyone running Claude Code on a large project: the agent burns through tokens doing file discovery, often spending more time exploring than coding. CodeGraph measured this exactly — across six real-world repos including VS Code, Excalidraw, and the Swift Compiler, unassisted Claude Code averaged 40+ tool calls just for navigation. With CodeGraph's MCP server active, agents needed 3–6 calls for the same tasks: a 92% reduction on average, and 71% faster wall-clock time.

The May 19 release of v0.7.10 fixed a critical bug where the MCP initialize handshake would time out on slow filesystems like Docker Desktop VirtioFS, leaving tools invisible to agents — exactly the kind of silent failure that kills adoption. The project also shipped a multi-agent installer in v0.7.7 that auto-configures Claude Code, Cursor, Codex CLI, and opencode in a single interactive prompt, eliminating the main friction point.

The timing is sharp: as Claude Code usage has spiked, so has the pain of long context sessions on large codebases. CodeGraph landed squarely in that gap.

## Key Features

- **92% fewer tool calls on average** — measured across 6 real-world codebases; VS Code hit 94% reduction, Swift Compiler 84%
- **19+ language support** — TypeScript, Python, Go, Rust, Java, C#, Swift, Kotlin, Dart, and more via tree-sitter
- **MCP-native interface** — exposes symbol search, call graph tracing, impact radius analysis, and context building as MCP tools
- **100% local** — no external API calls, no data transmitted; single SQLite file per project
- **Auto-sync** — native OS file watchers with debounced reindex keep the graph fresh as you code

## Quick Start

```bash
npx @colbymchenry/codegraph
```

The interactive installer detects which agents you use (Claude Code, Cursor, Codex CLI, opencode) and auto-configures each one. For existing projects, run `codegraph init -i` inside the project directory.

## The Verdict

If you run Claude Code daily on codebases larger than a few hundred files, this is a near-mandatory install — the 92% reduction in tool calls is simultaneously a speed boost, a token cost reduction, and a context budget win. Teams fighting token limits on large monorepos should treat it as infrastructure. Skip it if you're on small greenfield projects where Claude navigates fine without help; the index overhead won't pay off there.

📎 [GitHub](https://github.com/colbymchenry/codegraph) · [npm](https://www.npmjs.com/package/@colbymchenry/codegraph) · [Issues](https://github.com/colbymchenry/codegraph/issues)