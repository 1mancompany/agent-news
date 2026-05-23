---
title: "🔥 Hot Repo: Anthropic Just Built an App Store for Claude Code"
author: OMC Editorial
published_at: 2026-05-22T13:17:29.812853+00:00
slug: hot-repo-claude-plugins-official
image: https://opengraph.githubassets.com/1/anthropics/claude-plugins-official
source: https://news.one-man-company.com/news/hot-repo-claude-plugins-official
---

> **One-liner** — Anthropic's official plugin marketplace for Claude Code, bundling MCP servers, slash commands, agents, and skills installable with a single in-editor command.

- **Repo:** [anthropics/claude-plugins-official](https://github.com/anthropics/claude-plugins-official)
- **Stars:** ⭐ 23,819 (+2,556 today)
- **Language:** Python / TypeScript
- **License:** See individual plugins

---

## What It Does

`claude-plugins-official` is Anthropic's curated plugin directory for Claude Code, combining 35+ internal Anthropic-built plugins and 14+ vetted external partner plugins into a single, in-editor marketplace. Each plugin can bundle MCP servers, custom slash commands, agent definitions, and skills — giving Claude Code capabilities that used to require manual CLAUDE.md wiring and separate MCP configs. The repository was pushed today and continues to see rapid plugin additions from both Anthropic and external partners.

## Why It's Blowing Up

The repo surged to 23,819 stars (+2,556 in a single day, May 22) as Anthropic's plugin ecosystem matures and community submissions accelerate. Unlike the scattered third-party MCP server landscape, this directory is security-screened and maintained directly by Anthropic, giving enterprise teams a trusted source for extending Claude Code without auditing every JSON config manually. The 686 open issues and 2,710 forks signal a highly active developer community pushing new plugins through the approval pipeline.

The ecosystem flywheel is already spinning: external partners including Context7, Firebase, GitHub, GitLab, Linear, Asana, Terraform, and Playwright have shipped certified plugins, covering the most common developer toolchain integrations out of the box.

## Key Features

- **One-command install** — `/plugin install {plugin-name}@claude-plugins-official` adds any plugin in seconds without leaving the terminal
- **In-editor discovery** — Browse and install without leaving Claude Code via `/plugin > Discover`
- **35+ Anthropic-built plugins** — LSP integrations (Rust Analyzer, TypeScript, Python, Go, Swift, C#, Ruby, PHP) plus workflow tools (code-review, pr-review-toolkit, commit-commands, feature-dev)
- **14+ vetted partner plugins** — GitHub, Firebase, Terraform, Playwright, Linear, Asana, GitLab, Telegram, Discord, iMessage and more
- **Standardized plugin schema** — Every plugin ships a `.claude-plugin/plugin.json` manifest with optional `.mcp.json`, slash commands, agents, and skills

## Quick Start

```bash
# In Claude Code, install any plugin:
/plugin install github@claude-plugins-official
/plugin install playwright@claude-plugins-official
/plugin install terraform@claude-plugins-official

# Browse everything available:
/plugin
```

## The Verdict

If you use Claude Code seriously, this is the first place to check before wiring anything manually. The LSP plugins alone (TypeScript, Rust, Go, Swift, Python, C#, Lua, Ruby, PHP, Kotlin) remove a significant setup burden, and the GitHub, Linear, and Asana integrations mean you can manage repos and issues without leaving your terminal. It's not for developers who prefer hand-rolled MCP configs or who want to vet every dependency themselves — the external plugins require trusting Anthropic's screening process plus the third-party vendor. But for teams wanting battle-tested extensions with one-line installs, this is the Claude Code equivalent of the VS Code Extension Marketplace — and it's only getting bigger.

📎 [GitHub](https://github.com/anthropics/claude-plugins-official) · [Docs](https://code.claude.com/docs/en/plugins) · [Submit a Plugin](https://clau.de/plugin-directory-submission)