---
title: "🔥 Hot Repo: 2,500 Stars — The AI Browser No Bot Detector Can Touch"
author: OMC Editorial
published_at: 2026-10-03T13:10:40.517676+00:00
slug: hot-repo-dots-unblockable-browser
image: https://opengraph.githubassets.com/1/feder-cr/dots
source: https://news.one-man-company.com/news/hot-repo-dots-unblockable-browser
---

> **One-liner** — dots gives every AI agent a stealth Firefox browser that websites cannot detect as a bot — and it plugs straight into Claude Code, Codex, and any MCP client via a companion server.

- **Repo:** [feder-cr/dots](https://github.com/feder-cr/dots)
- **Stars:** ⭐ 2,567 (+~500 today)
- **Language:** Python
- **License:** MIT

---

## What It Does

dots is an open-source AI web agent built around one conviction: the browser is where agents fail, not the model. It ships a Firefox engine patched in C++ so the fingerprint is decided at the engine level — not layered on with detectable JavaScript. There is no WebDriver flag, no DevTools protocol, no automation globals. One `uvx` command installs it, `--model` swaps the LLM, and the agent opens a split-pane: conversation on the left, live browser on the right.

## Why It's Blowing Up

Commercial browser-agent platforms charge per-session fees or lock you into a single model. OpenAI's own Dots costs upward of $100/month. feder-cr/dots launched September 29 as an explicit open-source answer and hit 2,500 stars in four days. The timing lands squarely in the hottest problem space in AI automation: every pipeline that touches a web page eventually breaks on bot detection, and the community has been waiting for something that actually solves it at the engine level rather than papering over it.

Most "stealth" solutions inject JavaScript on top of a standard Chromium DevTools session — something pages can still inspect. dots patches Firefox itself in C++, baking the fingerprint in before any page script runs. The `--seed` flag locks a consistent identity (screen, fonts, GPU, timezone, language) across sessions, and `--profile-dir` carries logins and cookies from run to run. The `--proxy` flag goes further: it aligns the fingerprinted timezone and language with the proxy exit, so locale clues match geography.

## Key Features

- **C++-level stealth** — fingerprint decided inside the engine, no automation globals visible to page scripts
- **Model-agnostic** — any OpenRouter model; swap Claude, GPT-4o, or others with one `--model` flag
- **MCP server** — `invisible_playwright_mcp` exposes this browser to Claude Code, Codex, Gemini CLI, or any MCP-capable client
- **Persistent identity** — `--seed` for a repeatable persona; `--profile-dir` for session cookies and stored logins
- **Proxy-aware fingerprinting** — `--proxy` syncs timezone and language to the exit node

## Quick Start

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
source $HOME/.local/bin/env
uvx --from git+https://github.com/feder-cr/dots dots --openrouter-key sk-or-...
# Open http://127.0.0.1:8765 — conversation left, live browser right
```

## The Verdict

If you build AI automation that scrapes, monitors, or interacts with web pages, dots solves the part that actually breaks things. The C++ browser patching is not a gimmick: it tackles detection at the only layer that matters. The MCP integration means Claude Code gets a session-persistent, undetectable browser in two commands. Skip it if you need enterprise audit logs, managed uptime SLAs, or click-stream compliance — dots is a sharp local tool, not a service. For indie developers and teams self-hosting their agent stacks, this is the browser layer they have been waiting for.

📎 [GitHub](https://github.com/feder-cr/dots) · [MCP Server](https://github.com/feder-cr/invisible_playwright_mcp) · [The Daily Commit](https://thedailycommit.in/story/2026-09-30/04-github-feder-cr-dots)