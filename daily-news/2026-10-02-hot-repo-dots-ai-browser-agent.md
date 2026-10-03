---
title: "🔥 Hot Repo: 2,400 Stars and Websites Think It's Human"
author: OMC Editorial
published_at: 2026-10-02T13:12:06.849555+00:00
slug: hot-repo-dots-ai-browser-agent
image: https://opengraph.githubassets.com/1/feder-cr/dots
source: https://news.one-man-company.com/news/hot-repo-dots-ai-browser-agent
---

> **One-liner** — dots is an AI web agent built around a C++-patched Firefox whose fingerprint is set at the engine level, making it indistinguishable from a real human browser — and it wires directly into Claude Code, Codex, or any MCP client.

- **Repo:** [feder-cr/dots](https://github.com/feder-cr/dots)
- **Stars:** ⭐ 2,420 (+~800 today)
- **Language:** Python
- **License:** MIT

---

## What It Does

dots is a web agent that pairs any model on OpenRouter with a Firefox browser patched at the C++ source level — not with JavaScript overrides a page can detect. It launches a local web UI (conversation on the left, live browser on the right), and exposes the same browser as an MCP server for Claude Code, Codex, and Gemini CLI via the companion `invisible_playwright_mcp` package. A single `--seed` flag reproduces a consistent synthetic identity across runs; `--profile-dir` persists cookies and logins; `--proxy` aligns timezone and language with the exit node.

## Why It's Blowing Up

The timing is exact. In early 2026, Fingerprint shipped a product aimed specifically at classifying AI agent traffic — not bots in general, but AI agents as their own detection category. Standard Playwright and Puppeteer-based agents started failing at far higher rates. Camoufox, the last well-known C++-patched Firefox for anti-detection, had been in a maintenance gap for roughly a year with its base Firefox version several majors behind.

dots fills that vacuum. It ships Firefox 150 with weekly binary releases and achieves a measured 0.90 reCAPTCHA v3 score — compared to 0.1–0.3 for typical automated browser setups. The C++ patches cover GPU/WebGL, Canvas, audio, Navigator, WebRTC, and DevTools detection together: the only approach that holds up under tools that cross-correlate signals. The creator already maintains `invisible_playwright` (the core library), giving the repo a reputation and production user base from day one.

The viral hook was MCP: one `uvx` command gives Claude Code or Codex an undetectable browser as a tool call, and that one-liner circulated fast across Claude-focused communities.

## Key Features

- **C++ fingerprint patching** — browser identity baked into the engine, invisible to JavaScript probes
- **Seed-based identity** — `--seed N` reproduces consistent screen, fonts, GPU, timezone, and language
- **Human-like input** — pointer travels to click targets; keys press one at a time
- **MCP server mode** — `invisible_playwright_mcp` exposes dots as a tool server for any MCP client
- **Session persistence** — `--profile-dir` keeps logins and cookies across agent runs

## Quick Start

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
source $HOME/.local/bin/env
uvx --from git+https://github.com/feder-cr/dots dots --openrouter-key sk-or-YOUR_KEY
# Then open http://127.0.0.1:8765
```

## The Verdict

If you build AI agents that need to touch the real web — scraping prices, checking availability, logging into dashboards — dots is the only current open-source option that treats anti-detection as an engine problem rather than a JavaScript afterthought. The MCP integration makes it a one-line addition to Claude Code or Codex. Skip it for APIs that openly welcome crawlers; the overhead is not worth it. But if your agent keeps getting blocked, this is the repo.

📎 [GitHub](https://github.com/feder-cr/dots) · [MCP Server](https://github.com/feder-cr/invisible_playwright_mcp) · [PyPI](https://pypi.org/project/invisible-firefox/)