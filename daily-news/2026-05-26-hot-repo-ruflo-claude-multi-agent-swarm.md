---
title: "🔥 Hot Repo: 22M Downloads — Claude Code's Missing Agent Swarm Layer"
author: OMC Editorial
published_at: 2026-05-26T13:16:15.951018+00:00
slug: hot-repo-ruflo-claude-multi-agent-swarm
image: https://raw.githubusercontent.com/ruvnet/ruflo/main/ruflo/assets/ruflo-small.jpeg
source: https://news.one-man-company.com/news/hot-repo-ruflo-claude-multi-agent-swarm
---

> **One-liner** — Ruflo is an open-source orchestration layer that gives Claude Code a 100-agent swarm, persistent vector memory, and cross-machine federation — now natively supported on Windows as of v3.10.2.

- **Repo:** [ruvnet/ruflo](https://github.com/ruvnet/ruflo)
- **Stars:** ⭐ 55,306
- **Language:** TypeScript
- **License:** MIT

---

## What It Does

Ruflo wraps Claude Code with a multi-agent coordination layer: one `npx ruflo init` installs 98 named agents (architect, coder, test engineer, security auditor, and more), wires in a self-learning memory system backed by HNSW vector embeddings, and exposes 314 MCP tools for swarm coordination. Agents run concurrently across tasks, share memory across sessions, and improve from each successful pattern via the SONA learning loop. Federation support lets agent swarms span multiple machines with mTLS authentication and automatic PII stripping.

## Why It's Blowing Up

Ruflo (rebranded from Claude Flow in January 2026 to address trademark considerations) just shipped v3.10.2 on May 25 with fully native Windows support — removing the single biggest barrier to enterprise adoption. Previously, Windows users needed WSL or Git Bash to run plugin hooks; the release replaces bash shims with cross-platform Node.js equivalents validated on a Ubuntu + macOS + Windows CI matrix.

The scale tells the real story: 22.2M+ ecosystem downloads and 115K git clones in the past 14 days. Benchmarks pit Ruflo against LangGraph, AutoGen, and CrewAI on cold-start time, single-turn latency, and memory footprint — Ruflo wins by factors from 1.3× to 1,953×. Developers tired of orchestrating agents manually are converging on Ruflo because `npx ruflo init` is the only setup step required.

The timing is right: as Claude Code matures as a platform, Ruflo fills the coordination gap that Anthropic hasn't yet addressed natively — shared memory, parallel swarms, and cross-session learning that persists beyond a single conversation.

## Key Features

- **100+ Specialized Agents** — pre-built roles including coder, tester, architect, security auditor, and docs writer running concurrently
- **Self-Learning Memory** — HNSW-indexed AgentDB with 150x–12,500x faster search; agents recall successful patterns across sessions
- **Cross-Machine Federation** — agents on different servers collaborate via mTLS, automatic PII stripping, and behavioral trust scoring
- **33 Claude Code Plugins** — RAG memory, browser automation (Playwright), test generation, cost tracking, and more via `/plugin install`

## Quick Start

```bash
npx ruflo@latest init wizard
```

Or add as an MCP server directly in Claude Code:

```bash
claude mcp add ruflo -- npx ruflo@latest mcp start
```

## The Verdict

Ruflo is for teams already shipping with Claude Code who want to parallelize agent work and retain memory across sessions. The benchmarks and adoption numbers are compelling, and the 33-plugin ecosystem covers most production needs out of the box. It is not for beginners — 26 CLI commands and 314 MCP tools will overwhelm anyone not already comfortable with agentic workflows. The v3.10.2 Windows native fix is overdue and removes the main enterprise objection. If you're scaling Claude usage beyond one-off sessions, this is worth a star and a proper eval.

📎 [GitHub](https://github.com/ruvnet/ruflo) · [NPM](https://www.npmjs.com/package/ruflo) · [Web UI](https://flo.ruv.io/) · [Docs](https://github.com/ruvnet/ruflo/wiki/)