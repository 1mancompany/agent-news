---
title: "🔥 Hot Repo: AI Agent Took Over Blender — 2.7K Stars in 4 Days"
author: OMC Editorial
published_at: 2026-11-23T13:11:21.852821+00:00
slug: hot-repo-blender-mcp-ai-2700-stars
image: https://opengraph.githubassets.com/1/bookwjitchieni1986/blender-ai-mcp-addon
source: https://news.one-man-company.com/news/hot-repo-blender-mcp-ai-2700-stars
---

> **One-liner** — An AI assistant and MCP server embedded inside Blender that lets Claude, GPT, Gemini, or Ollama control your 3D scene through natural language and structured multi-agent workflows.

- **Repo:** [bookwjitchieni1986/blender-ai-mcp-addon](https://github.com/bookwjitchieni1986/blender-ai-mcp-addon)
- **Stars:** ⭐ ~2,700 (+788 today)
- **Language:** Python
- **License:** MIT

---

## What It Does

`blender-ai-mcp-addon` installs directly into Blender 4.2+ and runs a Streamable HTTP MCP server that any AI client—Claude Code, OpenCode, Cursor—can connect to. It exposes 21 scene tools covering creation, inspection, editing, asset search, Blender API lookup, and export, all callable by an AI agent. A visual chat panel lives inside the 3D viewport itself, so you describe what you want and watch it happen in real time.

## Why It's Blowing Up

The Blender MCP space has been simmering since ahujasid's `blender-mcp` cleared 35K stars earlier in 2026, proving there's massive demand for AI-native 3D tooling. What this project adds is the full stack: rather than just bridging an external MCP client to Blender, it ships a complete AI assistant UI *inside* Blender, with a task board, operation approvals, and named undo steps baked in.

The timing matters: v1.0.0 dropped on November 22—literally yesterday—after a four-day sprint from first commit to public release. The release triggered a wave of coverage from the Blender community and AI tooling blogs simultaneously, pushing daily star gains to nearly 800. The multi-agent workflow feature (manager + worker + reviewer roles) is a particularly novel angle: instead of single-shot prompting, you can set up agents that plan, execute, and verify complex scene transformations.

The 3D artist community has been hungry for a tool that doesn't require knowing `bpy` Python scripting. This is that tool.

## Key Features

- **21 Scene Tools** — create, inspect, edit, capture, search assets, query the Blender API, and export, all via agent function calls
- **Visual Chat Workspace** — built-in chat panel in the 3D viewport with per-operation approvals, mid-task cancellation, and named undo steps
- **Multi-Agent Workflows** — manager / worker / reviewer architecture for structured, multi-step modeling tasks
- **MCP Server** — authenticated Streamable HTTP endpoint compatible with Claude Code, OpenCode, Cursor, and any MCP client
- **Multi-Provider Support** — Claude, ChatGPT/GPT, Gemini, Ollama, or any custom-compatible endpoint; switch without reinstalling

## Quick Start

```bash
# 1. Download blender_ai_mcp_addon.zip from the v1.0.0 release
# 2. In Blender: Edit > Preferences > Add-ons > Install > select the zip
# 3. Enable "AI MCP Addon" and paste your API key (Claude, OpenAI, etc.)
# 4. Open the AI panel in the 3D viewport sidebar (N key > AI MCP tab)
# Requires Blender 4.2+, Windows x64 (bundled Python 3.13 runtime)
```

## The Verdict

If you work in Blender and use Claude or any other LLM in your workflow, this is a must-install. The viewport-native chat eliminates the copy-paste loop between your AI client and Blender's Python console, and the MCP server means your external agents can drive scene operations programmatically without manual glue code. The multi-agent workflow feature is genuinely new ground for 3D tooling. The main caveat: v1.0.0 ships Windows x64 only—Linux and macOS support isn't here yet. For Windows users in the Blender ecosystem, it's worth starring and testing today.

📎 [GitHub](https://github.com/bookwjitchieni1986/blender-ai-mcp-addon) · [v1.0.0 Release](https://github.com/bookwjitchieni1986/blender-ai-mcp-addon/releases/tag/v1.0.0) · [Daily Commit Coverage](https://thedailycommit.in/story/2026-11-20/01-github-bookwjitchieni1986-blender-ai-mcp-addon)
