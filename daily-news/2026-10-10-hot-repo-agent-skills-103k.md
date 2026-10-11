---
title: "🔥 Hot Repo: 103K Stars — Addy Osmani Wired Senior Engineering Into Claude Code"
author: OMC Editorial
published_at: 2026-10-10T13:16:05.711619+00:00
slug: hot-repo-agent-skills-103k
image: https://addyosmani.com/assets/images/addys-agent-skills.jpg
source: https://news.one-man-company.com/news/hot-repo-agent-skills-103k
---

> **One-liner** — agent-skills is a 25-skill, 9-command production engineering pack for AI coding agents that encodes the workflows, quality gates, and best practices that senior engineers use, so agents consistently spec, plan, build, verify, review, and ship — without the shortcuts.

- **Repo:** [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills)
- **Stars:** ⭐ 103,000 (+21K since August 2026)
- **Language:** Markdown / JavaScript
- **License:** MIT

---

## What It Does

agent-skills packages 25 production engineering workflows into Markdown skill files that Claude Code, Cursor, Codex, Copilot, and 70+ other AI agents load as context. Each skill encodes a specific lifecycle stage — from `spec-driven-development` before a line is written to `git-workflow-and-versioning` and `shipping-and-launch` at the end. Nine slash commands (/spec, /plan, /build, /test, /constraints, /review, /webperf, /code-simplify, /ship) map to each phase, and skills activate automatically based on what the agent is doing.

## Why It's Blowing Up

The core insight driving the repo's growth is one the author — Addy Osmani, formerly Google's Chrome DevRel lead — made plain in several posts: prompts are not the point. What separates a senior engineer's output from a junior's isn't what they ask; it's the disciplined process they run automatically — writing a spec before touching code, committing atomically, proving correctness with tests before calling anything done. Skills encode that discipline so agents run it consistently, not occasionally.

The project has grown from 45K to 103K stars since June 2026, fueled by a simple dynamic: every "my AI agent wrote broken code" complaint is a testimonial. Version 0.6.2 introduced the headline feature — `/build auto`. Approve the plan once, and the agent generates, tests, and commits every task without human steering between steps. It pauses on failures or risky actions; everything else runs autonomously. For teams running long Claude Code sessions, this is the shift from "supervise every step" to "review the final PR."

The repo has returned to GitHub Trending multiple times — most recently in early October 2026 — and was cited in several roundup articles as the benchmark for what a production-quality Claude Code skill pack should look like.

## Key Features

- **`/build auto` mode** — approve the plan once; the agent implements, tests, and commits every task autonomously, pausing only on failures or risky steps
- **25 skills across the full dev lifecycle** — spec, plan, build, verify, review, and ship, each a standalone installable workflow
- **`/constraints` command** — interviews you for quality thresholds, writes `CONSTRAINTS.md`, and catches agents silencing checks to get green
- **4 specialist agent personas** — code-reviewer, test-engineer, security-auditor, and web-performance-auditor for targeted reviews
- **Anti-rationalization built in** — every skill includes a table of excuses agents use to skip steps with documented counter-arguments

## Quick Start

```bash
npx skills add addyosmani/agent-skills   # installs all 25 skills into Claude Code, Cursor, Codex, and 65+ agents
```

Or as a native Claude Code plugin:

```bash
/plugin marketplace add addyosmani/agent-skills
/plugin install agent-skills@addy-agent-skills
```

## The Verdict

If you've watched Claude Code sail through a task only to produce code that skips tests, assumes rather than proves correctness, or generates 300-line files for 50-line problems — this is the fix. Each skill is a process with hard checkpoints the agent can't talk its way past. The `/build auto` mode is the payoff: define what to build, approve the breakdown, and come back to a PR with every slice tested and committed. Skip it only if your agent sessions are exploratory throwaway code where process adds friction with no benefit. For anything production-bound, it's the highest-ROI Claude Code install at zero cost.

📎 [GitHub](https://github.com/addyosmani/agent-skills) · [Homepage](https://skills.addy.ie/) · [Trendshift](https://trendshift.io/repositories/25200) · [DEV Community Review](https://dev.to/yimtheppariyapol/addy-osmani-agent-skills-review-24-production-skills-726k-stars-22em)