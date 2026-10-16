---
title: "🔥 Hot Repo: 144K Stars — Mix Claude and GPT in One Model Picker"
author: OMC Editorial
published_at: 2026-10-15T13:10:25.4042+00:00
slug: hot-repo-cc-switch-144k-mix-agents
image: https://opengraph.githubassets.com/1/farion1231/cc-switch
source: https://news.one-man-company.com/news/hot-repo-cc-switch-144k-mix-agents
---

> **One-liner** — CC Switch is a cross-platform desktop app that manages API providers, MCP servers, skills, and prompts across 10 AI coding tools — Claude Code, Codex, Gemini CLI, Grok Build, and six more — so you switch models and providers in one click instead of editing config files by hand.

- **Repo:** [farion1231/cc-switch](https://github.com/farion1231/cc-switch)
- **Stars:** ⭐ 144,622 (+~500 today)
- **Language:** Rust / TypeScript
- **License:** MIT

---

## What It Does

CC Switch is a Tauri 2 desktop app (Rust + TypeScript) that owns the config layer for 10 AI coding agents: Claude Code, Claude Desktop, Codex, Gemini CLI, Grok Build, OpenCode, OpenClaw, Hermes, Pi, and MiniMax Code. You configure API keys and provider presets once; it writes the right config for each tool. Its v4.0 headline feature — Aggregation mode — merges models from multiple providers into one picker inside Claude Code or Codex, routing each request directly to the provider behind the chosen model.

## Why It's Blowing Up

The problem CC Switch solves gets worse every month: there are now 10+ serious AI coding agents, each with its own config format, and most developers are running 2–4 of them simultaneously. Manually rotating API keys, swapping models, and syncing MCP server lists across Claude Code, Codex, and Gemini CLI compounds into a daily tax. CC Switch removes that tax by acting as a centralized control plane for all of them.

The project launched in August 2025 and grew from 89K to 144K stars in roughly two months, with October 2026 seeing fresh spikes after the v4.0 preview series dropped (v4.0.0–v4.0.4, October 4–6). Aggregation mode is the most-requested feature the project has shipped: pick `gpt-4.5` or `claude-sonnet-4-6` from the same menu inside Claude Code, without touching a config file.

V4.0 also rebuilt the config-writing engine to replace only key fields on a provider switch — endpoint, credential, model, protocol — leaving plugins, hooks, and comments intact. Previous versions rewrote the whole config file on switch, which was the top complaint in issue threads. The rebuilt session reader now supports nine clients with per-turn step summaries, failure markers, and Markdown export.

## Key Features

- **Aggregation Mode** — mix models from multiple providers in one Claude Code or Codex model picker; each request routes to the matching provider with no failover
- **90+ Provider Presets** — one-click switches across Anthropic, OpenAI, Gemini, and third-party endpoints; preserves plugins and hooks on every switch
- **MCP / Skills / Prompts Sync** — configure once and push to all 10 supported tools; v4.0 adds Pi (8 tools now covered via MCP sync)
- **Usage Tracking** — logs token counts, cost, and output speed per request with a 53-week heatmap and per-provider quota countdowns
- **Session Reader** — browse and search logs across 9 clients with turn-by-turn step summaries, changed-file lists, and Markdown export

## Quick Start

```bash
brew install --cask cc-switch
```

Linux (Arch):
```bash
paru -S cc-switch-bin
```

## The Verdict

If you run more than one AI coding agent — or rotate between Anthropic's native API and third-party Claude-compatible endpoints — CC Switch is the clearest win-per-minute install in the ecosystem right now. Aggregation mode is the genuine headline: choosing GPT-4.5 or Claude Sonnet from the same list inside Claude Code, without editing JSON, removes a friction layer that previously required separate workarounds per tool. Skip it only if you use exactly one agent on one provider with no plans to change either. MIT license and no-account-required setup keep enterprise adoption clean. Note: v4.0.0–v4.0.4 are still preview builds — for guaranteed stability, v3.20.4 (September 22) is the latest stable release.

📎 [GitHub](https://github.com/farion1231/cc-switch) · [Homepage](https://ccswitch.io) · [Usage Guide](https://qcode.cc/en/cc-switch-claude-code-guide)