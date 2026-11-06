---
title: "🔥 Hot Repo: 2,700 Stars in 48h — Claude Code's Missing Background Daemon"
author: OMC Editorial
published_at: 2026-11-05T13:14:08.640908+00:00
slug: hot-repo-agent-autoloop-2700-48h
image: https://opengraph.githubassets.com/1/KKKKhazix/agent-autoloop
source: https://news.one-man-company.com/news/hot-repo-agent-autoloop-2700-48h
---

> **One-liner** — Agent Autoloop is a zero-dependency TypeScript middleware that runs Claude Code, Codex, and any other CLI agent autonomously in the background, interrupting you only when it hits a decision it cannot make alone.

- **Repo:** [KKKKhazix/agent-autoloop](https://github.com/KKKKhazix/agent-autoloop)
- **Stars:** ⭐ ~2,700 (+2,700 in 48 hours)
- **Language:** TypeScript
- **License:** MIT

---

## What It Does

Most developers use Claude Code or Codex the same way: type a prompt, stare at the terminal, wait for the next question. Close the window, and the work stops. Agent Autoloop breaks that pattern. It sits between you and your CLI agent as a lightweight event-driven kernel: tasks come in via cron, GitHub webhook, or HTTP endpoint, get dispatched to whichever agent and working directory your rules say, and the agent runs until it hits something requiring human judgment — deleting data, spending money, pushing to prod. At that point it sends a card on Feishu, Slack, Discord, or desktop notification and stops spending tokens until you decide.

## Why It's Blowing Up

The repo launched on November 3, 2026 — two days ago — with v1.0.0 already at stable. Within 24 hours, seven community forks appeared, each adding minor variations. That forking velocity before a repo even has 48 hours of history is the strongest adoption signal in this category: developers are actively building on it, not just starring it.

The timing is exactly right. Claude Code and Codex now handle multi-step tasks well unattended — but only if the terminal stays open and you're watching. Teams have been cobbling together tmux sessions and ad-hoc wrappers to work around this. Agent Autoloop replaces all of that with a 1,650-line zero-runtime-dependency kernel, rules declared in `rules.json`, and a plugin architecture that makes event sources, agents, and notification channels swappable. The Windows version is pending (developer is on a work trip; ETA November 7-8), but macOS and Linux are fully supported today.

v1.1.0 landed in quick succession after v1.0.0, with the update mechanism now pinned to published releases rather than main — a signal that the project is stabilizing fast.

## Key Features

- **Background autonomy** — agents run without an open terminal; each task is a bounded "round" that exits after recording its result, consuming no tokens at rest
- **Decision-first interruptions** — sends a card via Feishu, Slack, Discord, or desktop only for sensitive actions; waits silently until you respond
- **rules.json dispatcher** — declare what event triggers which agent in which directory; changes take effect within seconds, no restart needed
- **Plugin ecosystem** — swappable event sources (GitHub/GitLab webhooks, cron, HTTP), agents (Claude Code, Codex, ACP, DeepSeek Harness, any CLI tool), and notification channels
- **Zero runtime dependencies** — 1,650-line kernel with no external packages at runtime

## Quick Start

```bash
curl -fsSL https://raw.githubusercontent.com/KKKKhazix/agent-autoloop/main/install.sh | sh
agent-autoloop try   # run a full test loop on your machine
```

Requires Node 24, Git, curl, and at least one already-signed-in CLI agent. No cloud account or inbound ports required.

## The Verdict

If you run Claude Code or Codex for tasks that take longer than a few minutes — refactoring, triaging issues, writing summaries, monitoring — Agent Autoloop is the most direct fix for the "babysitting a terminal" problem available today. The rules.json model takes five minutes to set up, and the plugin architecture lets you wire in GitHub webhooks, Slack, and CI/CD without touching the core. Skip it if you're on Windows (wait until November 7-8), or if your tasks need constant back-and-forth and can't be decomposed into autonomous rounds. For everything else: install it, write a cron rule, and walk away.

📎 [GitHub](https://github.com/KKKKhazix/agent-autoloop) · [v1.0.0 Release](https://github.com/KKKKhazix/agent-autoloop/releases/tag/v1.0.0) · [v1.1.0 Release](https://github.com/KKKKhazix/agent-autoloop/releases/tag/v1.1.0)