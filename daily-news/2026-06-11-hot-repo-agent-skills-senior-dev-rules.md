---
title: "🔥 Hot Repo: 53K Stars — The Pack Forcing AI Agents to Code Like Seniors"
author: OMC Editorial
published_at: 2026-06-11T13:11:23.524307+00:00
slug: hot-repo-agent-skills-senior-dev-rules
image: https://addyosmani.com/assets/images/addys-agent-skills.jpg
source: https://news.one-man-company.com/news/hot-repo-agent-skills-senior-dev-rules
---

> **One-liner** — `addyosmani/agent-skills` packages 24 production-grade engineering workflows into slash commands so AI coding agents stop skipping specs, tests, and security reviews.

- **Repo:** [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills)
- **Stars:** ⭐ 53,621 (+3,275 today)
- **Language:** Shell / Markdown
- **License:** MIT

---

## What It Does

Agent Skills is a collection of 24 structured skill files — plain Markdown with front matter — encoding the workflows senior engineers follow across the full dev lifecycle. Seven slash commands (`/spec`, `/plan`, `/build`, `/test`, `/review`, `/code-simplify`, `/ship`) map to development phases and activate the right skills automatically. Skills also fire contextually: designing an API triggers `api-and-interface-design`, building UI triggers `frontend-ui-engineering`, and so on.

## Why It's Blowing Up

The repo dropped v0.6.2 today (June 11) with notable additions: a new `web-performance-auditor` persona with a `/webperf` command, a dedicated observability-and-instrumentation skill, expanded security coverage for SSRF and LLM-specific vulnerabilities, and native Antigravity CLI support. The release also fixed a marketplace install path bug that had been blocking Claude Code plugin users since the previous version.

The timing lands in the middle of what developers are calling the "skills boom" — five of the top-20 GitHub trending repos today carry "skills" in the name, a format popularized by the Claude Code plugin ecosystem. What separates agent-skills from the pile is the author's track record: Addy Osmani is Google's Chrome engineering lead, and the skills are grounded directly in Google's engineering culture — Hyrum's Law in API design, the Beyoncé Rule in testing, trunk-based development in git workflow, and code-as-liability thinking in deprecation.

Multi-tool reach matters too. The same Markdown skill files install into Claude Code's plugin marketplace, Cursor rules, Gemini CLI, GitHub Copilot, Codex, Windsurf, OpenCode, and anything that accepts a system prompt. One pack, every agent.

## Key Features

- **7 lifecycle slash commands** — `/spec` through `/ship`, each activating contextual skills automatically
- **Anti-rationalization tables** — every skill debunks common agent excuses like "I'll add tests later"
- **4 specialist agent personas** — code reviewer, test engineer, security auditor, web performance auditor
- **Cross-agent compatibility** — single Markdown files install across Claude Code, Cursor, Gemini CLI, Codex, and more

## Quick Start

```bash
# Claude Code (marketplace install)
/plugin marketplace add addyosmani/agent-skills
/plugin install agent-skills@addy-agent-skills
```

## The Verdict

If you use AI coding agents daily and have watched them skip steps, paper over tests, or ship without security reviews — this pack directly targets that failure mode. The process-over-prose design (steps, checkpoints, and exit criteria rather than essays) is what makes it actually stick in practice. Not for teams that want AI to move without any guardrails; very much for teams that want AI to move fast without accumulating a maintenance tax. Worth starring even if you only pull one or two skill files.

📎 [GitHub](https://github.com/addyosmani/agent-skills) · [Blog Post](https://addyosmani.com/blog/agent-skills/) · [HN Discussion](https://news.ycombinator.com/item?id=48015397)