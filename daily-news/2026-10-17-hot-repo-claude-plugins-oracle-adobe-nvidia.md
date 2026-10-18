---
title: "🔥 Hot Repo: Oracle, Adobe & NVIDIA Are All Building Claude Code Plugins Now"
author: OMC Editorial
published_at: 2026-10-17T13:09:19.622484+00:00
slug: hot-repo-claude-plugins-oracle-adobe-nvidia
image: https://opengraph.githubassets.com/1/anthropics/claude-plugins-official
source: https://news.one-man-company.com/news/hot-repo-claude-plugins-oracle-adobe-nvidia
---

> **One-liner** — anthropics/claude-plugins-official is Anthropic's official Claude Code plugin marketplace — a curated directory of production-ready skills, MCP integrations, and language servers now carrying daily contributions from Oracle, Adobe, NVIDIA, Shopify, Zoom, and 40+ other enterprises.

- **Repo:** [anthropics/claude-plugins-official](https://github.com/anthropics/claude-plugins-official)
- **Stars:** ⭐ 41,189 (+~290 per day, +3,800 since Oct 4)
- **Language:** Python
- **License:** Apache-2.0

---

## What It Does

anthropics/claude-plugins-official is the curated app store for Claude Code. Plugins live as versioned folders that Claude Code installs with a single command or via the `/plugin > Discover` UI. The repo splits into two directories: `/plugins` for Anthropic-maintained tools (40+ currently, ranging from LSP language servers to MCP tunnel helpers), and `/external_plugins` plus an enterprise partner layer for third-party integrations — GitHub, GitLab, Firebase, Linear, Oracle AI Platform, NVIDIA, Adobe, Shopify, Slack, Zoom, and dozens more.

## Why It's Blowing Up

The most revealing stat isn't the 41K star count — it's the PR number. The most recent automated plugin update carried PR **#6713**. This repo has processed over 6,700 pull requests in less than a year, roughly 20 PRs per day every day since its August 2026 public launch. Each PR bumps a specific plugin to a new upstream commit hash, keeping every Claude Code installation in the ecosystem automatically current.

Enterprise adoption accelerated into October. Yesterday's automated batch alone updated plugins for Oracle AI Platform (three tools: Spark connectors, engineer agent, and Databricks migrator), NVIDIA skills, Adobe for Creativity, Shopify AI Toolkit, Zoom, Slack, Dropbox, Canva, SonarQube, DataRobot, and a half-dozen more. These aren't hobby projects — they're maintained by the companies themselves and updated daily.

A second catalyst hit in early October: the addition of a full LSP plugin collection. Claude Code can now wire up production language servers for 12 languages (TypeScript, Rust, Go, Python, C#, Java, Kotlin, Lua, PHP, Ruby, Swift, and Clang) with a single install. For developers who want Claude Code to have the same real-time diagnostic feedback an IDE provides, this closed the most-complained-about gap in the ecosystem — and the resulting discussion surge on HN and Reddit drove the jump from 37.4K to 41K stars in 13 days.

## Key Features

- **12 LSP plugins** — TypeScript, Rust, Go, Python, C#, Java, Kotlin, Lua, PHP, Ruby, Swift, and Clang language servers wired directly into Claude Code
- **mcp-tunnels** — connects Claude Code to MCP servers running inside private networks via an Anthropic-managed Cloudflare tunnel (research preview)
- **hookify** — create custom hooks that block unwanted agent behaviors using Markdown files with YAML frontmatter; no code required
- **Enterprise integrations** — Oracle AI Platform (3 tools), NVIDIA, Adobe, Shopify, Slack, Zoom, and Dropbox all ship daily-maintained plugins
- **External dev platforms** — GitHub, GitLab, Firebase, Linear, Terraform, Playwright, and Asana available via `/external_plugins`

## Quick Start

```bash
claude plugin install typescript-lsp@claude-plugins-official
```

To browse the full catalog inside Claude Code:

```bash
claude plugin discover
```

## The Verdict

If you run Claude Code for real work, this is the repo you should have bookmarked, not just starred. The LSP plugin collection alone closes the gap between Claude Code and traditional IDEs for real-time error feedback, and the enterprise plugin layer — Oracle, NVIDIA, Adobe, Shopify updating daily — signals that `claude-plugins-official` has become the canonical distribution channel for the Claude Code ecosystem. The main caveat: with 1,164 open issues and no formal release versioning, plugin quality varies. The repo itself warns that Anthropic cannot verify third-party plugin contents, so vet before installing. For anyone building seriously on Claude Code: this is where the ecosystem lives now.

📎 [GitHub](https://github.com/anthropics/claude-plugins-official) · [Plugin Docs](https://code.claude.com/docs/en/plugins) · [Claude Code Changelog](https://code.claude.com/docs/en/changelog)