---
title: "🔥 Hot Repo: 96K Stars — Claude Code Finally Has Memory"
author: OMC Editorial
published_at: 2026-10-05T13:08:31.620164+00:00
slug: hot-repo-claude-mem-96k-stars
image: https://opengraph.githubassets.com/1/thedotmack/claude-mem
source: https://news.one-man-company.com/news/hot-repo-claude-mem-96k-stars
---

> **One-liner** — claude-mem is a memory compression engine that hooks into Claude Code sessions, stores every observation in a local SQLite + ChromaDB hybrid database, and automatically re-injects the relevant context when the next session opens — so Claude never starts a project from scratch again.

- **Repo:** [thedotmack/claude-mem](https://github.com/thedotmack/claude-mem)
- **Stars:** ⭐ 96,389 (+628 today)
- **Language:** TypeScript
- **License:** Apache-2.0

---

## What It Does

claude-mem hooks into five lifecycle events (SessionStart, UserPromptSubmit, PostToolUse, Stop, SessionEnd) and streams every tool call, decision, and observation to a local HTTP worker. That worker indexes the data in SQLite with FTS5 full-text search and a local ChromaDB vector store. When a new session opens, a hybrid keyword + semantic search surfaces only the most relevant memory chunks — and injects them before you type a single prompt, giving Claude immediate project context.

## Why It's Blowing Up

Claude Code shipped in 2025 with no native cross-session memory. Every time a session ends, Claude starts over: it doesn’t know the architecture you explained last Tuesday, the bug you spent three hours chasing, or the team conventions already agreed on. That blank slate costs real time — and the pain scales directly with project complexity, exactly where agentic coding is most valuable.

claude-mem launched in August 2025 and crossed 96K stars in just 13 months. The 8,510 forks are the more telling number: teams aren’t just starring this, they’re integrating it into production workflows. Engineering leads have cited it as the reason their Claude Code sessions “finally feel like a senior dev who actually remembers the project.”

The timing also aligns with Claude Code spreading into enterprise teams and growing past 149K stars of its own. As sessions get longer and codebases more complex, the memory gap becomes the top productivity complaint — and claude-mem is the only open-source tool that addresses it across Claude Code, Cursor, Codex, Gemini, Copilot, Hermes, and OpenCode from a single install.

## Key Features

- **Five Lifecycle Hooks** — captures SessionStart, UserPromptSubmit, PostToolUse, Stop, and SessionEnd events automatically with no manual instrumentation
- **Hybrid Memory Search** — SQLite FTS5 keyword index + local ChromaDB vector store for accurate, low-latency retrieval
- **Progressive Disclosure** — layered retrieval shows token cost at each memory tier so you can tune context budget before a session
- **Privacy Controls** — wrap any content in `<private>` tags to exclude sensitive details from the memory store entirely
- **Web Viewer UI** — real-time memory stream visualization in a browser interface so you can inspect and curate what Claude retains

## Quick Start

```bash
npx claude-mem install
```

## The Verdict

If you run Claude Code on anything longer than a 30-minute throwaway task, claude-mem is close to a must-install. The problem it solves — rebuilding project context from zero every session — is universal and the cost compounds daily. Apache-2.0 keeps enterprise use clean. The one friction point is the local ChromaDB dependency, which requires Node 20+ and a running worker process. Skip it if you only run brief isolated sessions; install it the moment Claude Code is part of a real multi-day project.

📎 [GitHub](https://github.com/thedotmack/claude-mem) · [npm](https://www.npmjs.com/package/claude-mem) · [Vibeindex](https://vibeindex.ai/collection/thedotmack/claude-mem)