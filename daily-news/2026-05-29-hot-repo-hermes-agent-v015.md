---
title: "🔥 Hot Repo: 172K Stars — The Agent That Outran Codex CLI"
author: OMC Editorial
published_at: 2026-05-29T13:13:23.990996+00:00
slug: hot-repo-hermes-agent-v015
image: https://raw.githubusercontent.com/NousResearch/hermes-agent/main/assets/banner.png
source: https://news.one-man-company.com/news/hot-repo-hermes-agent-v015
---

> **One-liner** — Nous Research's self-improving AI agent just shipped v0.15 with its 16K-line core shrunk 76%, session search made 4,500× faster, and a cold-start benchmark that now beats OpenAI's Codex CLI head-to-head.

- **Repo:** [NousResearch/hermes-agent](https://github.com/NousResearch/hermes-agent)
- **Stars:** ⭐ 172,390 (+est. 1,200 today)
- **Language:** Python
- **License:** MIT

---

## What It Does

Hermes Agent is an open-source, self-improving AI agent from Nous Research that runs on any infrastructure — $5 VPS, Docker, SSH, or serverless via Modal or Daytona. The core hook is a closed learning loop: the agent creates skills from experience, improves them during use, and builds a persistent cross-session model of who you are. Switch between 200+ models via `hermes model` with no code changes; talk from Telegram while it runs on a remote VM.

## Why It's Blowing Up

v0.15.0 "The Velocity Release" shipped May 28 with numbers that don't usually appear in a single release: 1,302 commits, 747 merged PRs, and 321 community contributors — the project's largest release ever. The headline refactor compressed `run_agent.py` from 16,083 lines to 3,821 (-76%) across 14 cohesive modules, with behavior identical and every test patch path preserved. The practical payoff shows in benchmarks: `hermes --version` now flips the head-to-head cold-start comparison against OpenAI's Codex CLI, with 47% fewer per-conversation function calls shaved off along the way.

The release also lands on the same week Anthropic shipped Opus 4.8 — and hermes-agent's GitHub topics include `claude-code` and `anthropic`. v0.15.0 adds Opus 4.8 support and ships a Nous-approved MCP catalog with an interactive picker, giving it a direct upgrade path for developers already running Claude Code. The Kanban multi-agent platform — built across 104 PRs — now supports full swarm topology: `hermes kanban swarm` creates a root, parallel workers, gated verifier, gated synthesizer, and shared blackboard in a single command. A Brainworm-class promptware defense layer rounds out the security story.

## Key Features

- **Closed Learning Loop** — FTS5 session search with LLM summarization is now 4,500× faster and free; agent auto-creates and self-improves skills from complex tasks
- **Kanban Swarm Platform** — `hermes kanban swarm` deploys swarm topology with per-task model overrides, scheduled start times, and worktree-per-task isolation
- **Model Agnostic** — 200+ models via OpenRouter, NVIDIA NIM, xAI, OpenAI, Nous Portal; swap with `hermes model`, no lock-in
- **MCP Catalog** — Interactive picker for Nous-approved MCP servers, added in v0.15.0 alongside Opus 4.8 support
- **Runs Anywhere** — Local, Docker, SSH, Singularity, Modal, Daytona; gateway supports Telegram, Discord, Slack, WhatsApp, Signal, and 19 other platforms
- **Promptware Defense** — v0.15.0 ships protection against Brainworm-class prompt injection attacks

## Quick Start

```bash
curl -fsSL https://raw.githubusercontent.com/NousResearch/hermes-agent/main/scripts/install.sh | bash
source ~/.bashrc
hermes
```

## The Verdict

If you're already running Claude Code or Codex CLI and want a self-hosted alternative with persistent memory, skill accumulation, and real multi-agent orchestration, Hermes Agent v0.15 is the strongest version yet. The 76% core refactor signals a team serious about long-term velocity, not just features. It's not for teams that need zero-setup SaaS or enterprise audit logs out of the box — but for any developer comfortable with a VPS and a model API key, this is worth starring and trying. The OpenClaw migration path (`hermes claw migrate`) makes switching friction-free.

📎 [GitHub](https://github.com/NousResearch/hermes-agent) · [Homepage](https://hermes-agent.nousresearch.com) · [v0.15.0 Release Notes](https://github.com/NousResearch/hermes-agent/releases/tag/v2026.5.28)