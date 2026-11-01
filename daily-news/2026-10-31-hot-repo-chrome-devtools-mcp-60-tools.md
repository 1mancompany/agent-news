---
title: "🔥 Hot Repo: Google's 60-Tool MCP Ends Browser Blindness for AI Agents"
author: OMC Editorial
published_at: 2026-10-31T13:11:54.638903+00:00
slug: hot-repo-chrome-devtools-mcp-60-tools
image: https://opengraph.githubassets.com/1/ChromeDevTools/chrome-devtools-mcp
source: https://news.one-man-company.com/news/hot-repo-chrome-devtools-mcp-60-tools
---

> **One-liner** — ChromeDevTools/chrome-devtools-mcp is Google Chrome's official MCP server that gives AI coding agents full DevTools access to a live browser — from network inspection to heap snapshot analysis — without leaving the agent loop.

- **Repo:** [ChromeDevTools/chrome-devtools-mcp](https://github.com/ChromeDevTools/chrome-devtools-mcp)
- **Stars:** ⭐ 54,537
- **Language:** TypeScript
- **License:** Apache-2.0

---

## What It Does

`chrome-devtools-mcp` turns a live Chrome browser into a first-class tool for AI coding agents. Via the MCP protocol, agents can capture performance traces, analyze network requests, take source-mapped screenshots, run Puppeteer automation, and — since v1.12.0 — analyze heap snapshots entirely detached from a running browser, all through 60 tools organized into 12 groups. It ships as an MCP server, a standalone CLI, and a plugin installable in Claude Code, Cursor, Copilot, and Gemini CLI in a single command.

## Why It's Blowing Up

AI coding agents are increasingly expected to fix what they build, not just write it. The problem: most agents work blind — they can write code, run tests, and read logs, but have no visibility into a live browser. `chrome-devtools-mcp` closes that gap by giving agents the same debugging surface a human developer uses: Chrome DevTools itself.

The project hit v1.12.0 on October 22, 2026, adding offline heap snapshot analysis (no live browser required) and configurable navigation history limits. Google's October 2026 "New in DevTools" blog simultaneously highlighted new security controls — configurable filesystem roots and CLI path permissions — along with improved performance tuning for agent workflows. Coverage spread quickly across developer blogs and MCP tool registries, and it now lists 60 tools in 12 groups with an eSEOspace deep-dive clocking in on October 28.

What sets this apart from Playwright- or Puppeteer-based MCP servers: it speaks Chrome DevTools Protocol natively. That means agents get source-mapped stack traces, real-user CrUX field data alongside lab perf traces, memory profiles, cookie inspection, and full accessibility audits — not just "click and screenshot."

## Key Features

- **60 tools across 12 groups** — navigation, screenshots, network, performance, memory, accessibility, cookies, and more
- **Offline heap snapshot analysis** (v1.12.0) — profile memory without a running browser
- **7 built-in agent skills** — including `a11y-debugging`, `memory-leak-debugging`, and `debug-optimize-lcp`
- **One-command plugin install** — adds the server and all skills to Claude Code, Copilot, or Gemini CLI instantly

## Quick Start

```json
{
  "mcpServers": {
    "chrome-devtools": {
      "command": "npx",
      "args": ["-y", "chrome-devtools-mcp@latest"]
    }
  }
}
```

## The Verdict

If you use Claude Code, Cursor, or Copilot to build front-end or full-stack apps, this is the single most useful MCP server you're probably not running yet. It lets your agent actually debug what it builds — capturing real performance traces, hunting memory leaks, and fixing accessibility errors — instead of guessing from test output alone. Not relevant for pure back-end or CLI work, and requires Chrome installed on the host machine. For everyone building anything that runs in a browser: star it, drop it in your config, and watch your agent close its own bug tickets.

📎 [GitHub](https://github.com/ChromeDevTools/chrome-devtools-mcp) · [Chrome DevTools Blog](https://developer.chrome.com/blog/chrome-devtools-mcp) · [New in DevTools Oct 2026](https://developer.chrome.com/blog/new-in-devtools-october-2026)