---
title: "🔥 Hot Repo: 3.6M Downloads — One App to Rule Every AI CLI"
author: OMC Editorial
published_at: 2026-06-01T13:11:37.79678+00:00
slug: hot-repo-cc-switch-36m-downloads
image: https://raw.githubusercontent.com/farion1231/cc-switch/main/assets/screenshots/main-en.png
source: https://news.one-man-company.com/news/hot-repo-cc-switch-36m-downloads
---

> **One-liner** — CC Switch is a free, open-source desktop app that manages provider credentials, MCP servers, prompts, and Skills for Claude Code, Codex, Gemini CLI, OpenCode, OpenClaw, and Hermes Agent from a single cross-platform GUI.

- **Repo:** [farion1231/cc-switch](https://github.com/farion1231/cc-switch)
- **Stars:** ⭐ 87,591 (~500 today)
- **Language:** Rust / TypeScript (Tauri 2)
- **License:** MIT

---

## What It Does

CC Switch is a cross-platform desktop manager (Windows, macOS, Linux) for the expanding zoo of AI CLI tools. Instead of hand-editing , , and Gemini credential files, it gives you a GUI to add provider API keys, switch the active provider with one click or from the system tray, and sync MCP servers, system prompts, and Skills extensions across all six supported tools simultaneously.

## Why It's Blowing Up

Two forces are driving the star count. First, the AI CLI ecosystem is fragmenting fast — Claude Code, Codex, Gemini CLI, OpenCode, OpenClaw, and Hermes Agent each maintain separate credential files, so developers juggling multiple providers face constant manual config surgery. CC Switch is the only unified manager that covers all six at once.

Second, v3.16.0 (May 29) and today's v3.16.1 hotfix unlocked a genuinely novel capability: a local proxy that converts Codex's proprietary Responses API format into OpenAI Chat Completions in real time, enabling DeepSeek, Kimi, GLM, MiniMax, and 18 other Chat-format providers inside Codex with no native support required. The project ships 22 Chat-routing presets covering major Chinese and Asian LLM providers. Today's patch specifically hardened OAuth preservation — some users on v3.16.0 found their official ChatGPT login was being overwritten when switching to third-party Codex providers.

The traction numbers are hard to ignore: the five most recent releases have accumulated **3.6 million binary downloads**. v3.14.1 alone pushed nearly 1 million installer downloads before the next major release landed, and v3.16.0 crossed 250K downloads in under three days.

## Key Features

- **6-tool coverage** — single GUI for Claude Code, Codex, OpenCode, OpenClaw, Gemini CLI, and Hermes Agent
- **Codex Chat Completions proxy** — converts Responses API to Chat Completions on-the-fly, enabling DeepSeek/Kimi/GLM in Codex with full reasoning and tool-call passthrough
- **Unified MCP & Skills panel** — install MCP servers and Claude Code Skills from GitHub repos or ZIP files, synced bidirectionally across all apps
- **50+ provider presets** — AWS Bedrock, NVIDIA NIM, SiliconFlow, and dozens of community relay presets, importable with one click

## Quick Start

```bash
# macOS
brew install --cask cc-switch

# Windows
winget install farion1231.cc-switch
```

## The Verdict

If you run more than one AI CLI tool, CC Switch earns its spot in your menu bar immediately — the one-click provider switching alone eliminates a real papercut. The Codex Chat Completions routing is the standout feature: it fills a gap the official Codex client will not close anytime soon, and the 22 preset catalog means setup is near-zero. Caveats: the tool is heavily oriented toward users on third-party API relay plans rather than official subscriptions, and the repeated warnings about counterfeit sites charging for the free app signal that demand has outrun brand awareness. Recommended for any developer juggling multiple AI CLIs; less essential if you're locked to a single provider.

📎 [GitHub](https://github.com/farion1231/cc-switch) · [Website](https://ccswitch.io) · [Releases](https://github.com/farion1231/cc-switch/releases/latest)
