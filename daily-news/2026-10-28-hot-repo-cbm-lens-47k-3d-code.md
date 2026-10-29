---
title: "🔥 Hot Repo: 47K Stars — This MCP Gives Your AI Agent a 3D Code Brain"
author: OMC Editorial
published_at: 2026-10-28T13:20:04.71006+00:00
slug: hot-repo-cbm-lens-47k-3d-code
image: https://opengraph.githubassets.com/1/DeusData/codebase-memory-mcp
source: https://news.one-man-company.com/news/hot-repo-cbm-lens-47k-3d-code
---

> **One-liner** — codebase-memory-mcp is an MCP server that builds a persistent local knowledge graph of your entire codebase — code, docs, and infra — so AI coding agents can navigate and reason about large repos without burning tokens on repeated file reads.

- **Repo:** [DeusData/codebase-memory-mcp](https://github.com/DeusData/codebase-memory-mcp)
- **Stars:** ⭐ 47,701 (+~400 today)
- **Language:** C
- **License:** MIT

---

## What It Does

codebase-memory-mcp is a native C MCP server that indexes your repository into a persistent local graph database, connecting symbols, files, documentation, infrastructure configs, and architecture decisions. It exposes 17 MCP tools that let AI agents — Claude Code, Codex, Cursor, Windsurf, Gemini CLI, and 40 others — query structural context (callers, dependencies, semantic search, file impact) without constantly re-reading source files. Indexing and queries run entirely on your machine with no hosted service and no API key.

## Why It's Blowing Up

On October 20, 2026, DeusData shipped CBM Lens Beta v0.0.1 — an optional visual companion that renders the codebase knowledge graph in 3D. The "Galaxy" view lets developers follow call paths through three-dimensional space, while the architecture map groups symbols into nested components with dependency arrows. That visual launch landed at exactly the right moment: as AI coding agents have become a standard part of developer workflows in 2026, the question of how to give an agent structural context across a 100k-line codebase is urgent, and codebase-memory-mcp answers it with a graph-native approach rather than naive RAG.

The project has grown relentlessly since its February 2026 launch, sitting at the intersection of three converging trends: MCP standardization (with 45 agent integrations pre-configured at install), context engineering (its compression layer cuts 20–95% of token overhead on structured outputs), and local-first AI tooling (all indexing happens on-device). A peer-reviewed arXiv paper (2603.27277) adds unusual credibility, and SLSA 3 provenance, VirusTotal scanning on every release, and a strong OpenSSF Scorecard signal a security posture rarely seen in developer-tools repos.

## Key Features

- **Persistent Knowledge Graph** — indexes symbols, docs, infra configs, and architecture decisions into a local SQLite graph that survives between sessions and can be shared as a team baseline
- **17 MCP Tools** — symbol search, call graph traversal, file impact analysis, dependency queries, and change-aware test selection, all accessible via MCP
- **CBM Lens 3D (Beta)** — visual companion with Galaxy (3D call graph), architecture maps, coverage diagnostics, and a local AI chat over selected code
- **162 Languages** — tree-sitter-based parsing across 162 file and config types including Terraform, Helm, Kubernetes, Ansible, and CI configs
- **45 Agent Integrations** — auto-configures Claude Code, Codex, Cursor, Windsurf, Gemini CLI, Kiro, and more with durable skills, profiles, and applicable hooks

## Quick Start

```bash
curl -fsSL https://raw.githubusercontent.com/DeusData/codebase-memory-mcp/main/install.sh | bash
```

After installation, start CBM Lens with: `codebase-memory-mcp daemon start --open --port=9749`

## The Verdict

codebase-memory-mcp is for developers who are actively using AI coding agents on mid-to-large codebases and hitting the context wall — repeated file reads, lost structural understanding, hallucinated call paths. If your project is under 10k lines and you're mostly prototyping, it's overkill. But for anyone maintaining a real system with Claude Code, Codex, or Cursor, this is the missing layer: a local, persistent, zero-cost graph that makes your agent structurally aware of the entire codebase. CBM Lens Beta is still rough (v0.0.1), but the Galaxy view and architecture maps are already legitimately useful for navigating unfamiliar code. Star it.

📎 [GitHub](https://github.com/DeusData/codebase-memory-mcp) · [arXiv Paper](https://arxiv.org/abs/2603.27277) · [Discord](https://discord.gg/KguGXxg2X)