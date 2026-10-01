---
title: "🔥 Hot Repo: Boot a Claude-Codex Dev Team With One Command"
author: OMC Editorial
published_at: 2026-09-30T13:54:34.876616+00:00
slug: hot-repo-openrig-claude-codex-team
image: https://raw.githubusercontent.com/mvschwarz/openrig/main/assets/readme/openrig-agents-working.gif
source: https://news.one-man-company.com/news/hot-repo-openrig-claude-codex-team
---

> **One-liner** — OpenRig is a multi-agent harness that lets you define Claude Code and Codex teams in YAML and run them as a single, coordinated system from one command.

- **Repo:** [mvschwarz/openrig](https://github.com/mvschwarz/openrig)
- **Stars:** ⭐ 2,744 (+737 today)
- **Language:** TypeScript
- **License:** Apache-2.0

---

## What It Does

OpenRig manages the *system* AI coding agents form when you run them together — not the agents themselves. You define topologies in YAML (called RigSpecs), boot the whole team with `rig up`, and get a TUI showing every seat, its model, context usage, and runtime state. Agents communicate via `rig send`, `rig broadcast`, and shared chatrooms; the human steps in only for decisions.

## Why It's Blowing Up

The multi-agent coding wave hit critical mass in 2026. Developers found themselves juggling four terminal windows — a Claude Code session here, a Codex session there — with no coordination layer on top. OpenRig fills that gap, and the timing matches a surge in "agentmaxxing": running multiple AI coding agents from different vendors in parallel across isolated git worktrees.

A second driver is the "system-of-systems" pattern the community has been describing. Senior devs report running a dev pod (implementor + QA + design) alongside an adversarial review pod where Claude and Codex cross-check each other's work. OpenRig gives that pattern a proper harness instead of bash glue. The project was pushed today (September 30, 2026) and added 737 stars in 24 hours — outsized for a developer-infrastructure tool requiring tmux and Node.js 22.

The HN Show thread surfaced the core pitch clearly: it's designed to be driven by your agent, not by you typing commands by hand. That framing — the human as coordinator, not typist — resonates with how developers are actually working in 2026.

## Key Features

- **RigSpec YAML** — define pods, edges, and seats declaratively; OpenRig wires up the tmux sessions automatically
- **Mixed provider support** — same rig can hold Claude Code seats and Codex seats side by side
- **TUI topology view** — graph and table showing runtime, model, context, and state per seat in real time
- **Cross-agent messaging** — `rig send`, `rig broadcast`, and `rig chatroom` for coordinated work between seats
- **Snapshot + restore** — `rig down --snapshot` and `rig up <name>` to persist and resume full teams
- **Slack bridge** — experimental integration so agents can surface decisions to a Slack workspace

## Quick Start

```bash
npm install -g @openrig/cli
cd /path/to/your/repository
rig up first-project-mixed --cwd .
rig tui --shared
```

## The Verdict

OpenRig is for developers already running Claude Code or Codex who want to orchestrate multiple agents without writing bash glue or memorizing which tmux window is which. If you're happy in a single agent session, this is overkill — the setup requires tmux, Node.js 22, and at least one authenticated CLI. But if you're already "agentmaxxing" across multiple AI coding assistants, this is the coordination layer you've been duct-taping together yourself. Worth a star today; watch for a stable 1.0 before putting it in CI.

📎 [GitHub](https://github.com/mvschwarz/openrig) · [Homepage](https://openrig.dev) · [Discussions](https://github.com/mvschwarz/openrig/discussions)
