---
title: "🔥 Hot Repo: Anthropic Targets BigLaw With 12 Open-Source Legal AI Plugins"
author: OMC Editorial
published_at: 2026-05-25T13:13:55.936505+00:00
slug: hot-repo-anthropic-legal-plugins
image: https://opengraph.githubassets.com/1/anthropics/knowledge-work-plugins
source: https://news.one-man-company.com/news/hot-repo-anthropic-legal-plugins
---

> **One-liner** — Anthropic's official open-source plugin kit for Claude just expanded with 12 practice-area legal plugins and 20+ MCP connectors, giving law firms a ready-made Claude configuration that wires directly into the tools they already use.

- **Repo:** [anthropics/knowledge-work-plugins](https://github.com/anthropics/knowledge-work-plugins)
- **Stars:** ⭐ 14,671 (+1,448 today)
- **Language:** Python
- **License:** Apache-2.0

---

## What It Does

`knowledge-work-plugins` is Anthropic's official open-source repository of role-specific plugins for Claude Cowork and Claude Code. Each plugin bundles domain skills, MCP server connectors, and slash commands for a specific job function — covering sales, finance, engineering, data, bio-research, and now legal. The entire system is file-based (markdown + JSON), so there are no build steps and no infrastructure to run.

## Why It's Blowing Up

On May 12, 2026, Anthropic launched "Claude for Legal" — the most coordinated AI push into the legal market since Harvey AI emerged. The release packaged 12 practice-area plugins (Commercial, Corporate, M&A, Employment, Privacy, Product, Regulatory, AI Governance, IP, and Litigation Legal) alongside 22+ new MCP connectors, wiring Claude into the tools legal teams already use: Ironclad and DocuSign for contracts, Relativity and Everlaw for e-discovery, iManage and NetDocuments for document management, and Midpage, Trellis, and Legal Data Hunter (31M+ documents, 160+ jurisdictions) for legal research.

The legal drop was the headline event, but it's part of a broader pattern: the repo has grown from 11 plugins at launch in January 2026 to over 20, now spanning engineering, HR, design, small business, operations, and bio-research. Legal attracted the most coverage because, unlike productivity or sales tools, legal AI directly touches liability — and established players like Harvey, Relativity, and Thomson Reuters responded by integrating rather than competing.

The star spike also reflects a developer audience discovering the repo's architecture: everything is plain markdown and JSON. Fork a plugin, swap in your MCP server endpoints, add company playbooks and terminology, and you have a working domain-specific Claude configuration within hours.

## Key Features

- **12 legal practice-area plugins** — pre-configured workflows for Commercial, IP, Litigation, AI Governance, Employment, Privacy, and more
- **20+ MCP connectors** — native integrations with Ironclad, DocuSign, Relativity, iManage, Everlaw, Datasite, and Trellis
- **Slash commands** — each plugin ships with commands like `/review-contract`, `/triage-nda`, `/brief`, and `/respond`
- **File-based config** — all plugins are markdown + JSON; no code, no build system, no infrastructure

## Quick Start

```bash
# Add the official marketplace
claude plugin marketplace add anthropics/knowledge-work-plugins

# Install the legal plugin (or swap in: sales, finance, engineering, etc.)
claude plugin install legal@knowledge-work-plugins
```

## The Verdict

This is one of the most practically useful open-source AI repos of 2026 — not because it's technically impressive, but because it ships real enterprise context in a format any developer or team lead can edit in a text editor. Legal teams, ops teams, and engineers evaluating Claude Cowork should clone this before writing a single custom prompt. The main caveat: the legal plugins default to U.S. jurisdictions (you must configure `legal.local.md` for non-U.S. work), and the whole thing assumes you're already on Anthropic's stack. If you're not, this won't help you. If you are, it's the fastest path to production-ready enterprise AI by a wide margin.

📎 [GitHub](https://github.com/anthropics/knowledge-work-plugins) · [Claude Cowork](https://claude.com/product/cowork) · [Coverage](https://www.lawnext.com/2026/05/anthropic-goes-all-in-on-legal-releasing-more-than-20-connectors-and-12-practice-area-plugins-for-claude.html)