---
title: "🔥 Hot Repo: 51 Agents That Make Claude Code Smarter Every Sprint"
author: OMC Editorial
published_at: 2026-05-31T13:08:38.758386+00:00
slug: hot-repo-compound-engineering-plugin
image: https://opengraph.githubassets.com/1/EveryInc/compound-engineering-plugin
source: https://news.one-man-company.com/news/hot-repo-compound-engineering-plugin
---

> **One-liner** — Compound Engineering is an open-source Claude Code plugin that makes each coding session smarter than the last, codifying decisions, patterns, and learnings into reusable agent skills.

- **Repo:** [EveryInc/compound-engineering-plugin](https://github.com/EveryInc/compound-engineering-plugin)
- **Stars:** ⭐ 18,550 (+trending today)
- **Language:** TypeScript
- **License:** MIT

---

## What It Does

Compound Engineering packages 37 skills and 51 specialized agents into a single installable Claude Code plugin. Built by Every.to (the AI-focused media company run by Dan Shipper and Kieran Klaassen), it enforces a structured development loop: brainstorm → plan → work → review → compound. The `/ce-compound` command is the differentiator — it captures what the agent learned from each task so future agents start smarter, not blank.

## Why It's Blowing Up

Every.to built this plugin to run five products with primarily single-person engineering teams. The methodology flips the ratio most developers use: 80% of effort goes into planning and review, 20% into execution. Per independent benchmarks, that inversion drives 300–700% faster development velocity.

The repo is trending hard this weekend following a run of rapid releases — v3.9.3 dropped May 28 with a fix to `/ce-plan`'s external-research routing, part of 30 total releases shipped. That cadence signals production-tested, actively maintained code, not a proof-of-concept. The plugin now supports Claude Code, Cursor, Codex, GitHub Copilot, Factory Droid, and Qwen Code — zero barrier to entry regardless of your toolchain.

What's really driving the spike is that it solves a concrete frustration every AI-assisted dev hits: agents don't remember what they learned. Each new Claude Code session starts cold. Compound Engineering changes that by surfacing documented architectural decisions, past bug patterns, and reviewed code learnings as grounding context — each sprint genuinely builds on the last.

## Key Features

- **`/ce-brainstorm` + `/ce-plan`** — Interactive Q&A that turns rough ideas into right-sized requirements docs before any code is written
- **`/ce-compound`** — Captures per-task learnings as durable notes so future agents skip the same learning curve
- **`/ce-code-review`** — Multi-agent review pass that catches systemic patterns, not just individual bugs
- **`/ce-strategy`** — Maintains a `STRATEGY.md` anchor so product context flows automatically into every brainstorm and plan

## Quick Start

```bash
# In Claude Code
/plugin marketplace add EveryInc/compound-engineering-plugin
/plugin install compound-engineering
/ce-setup
```

## The Verdict

If you're shipping with Claude Code and not already on Compound Engineering, install it now — it's free, MIT-licensed, and the `/ce-compound` + `/ce-plan` loop alone will recoup the setup cost within a single sprint. It's not for developers who write one-off scripts or prefer zero ceremony; planning docs and compound notes add real friction for lightweight use. But for anyone running a product with an AI coding agent, this is the closest thing to a proven standard methodology the ecosystem has produced.

📎 [GitHub](https://github.com/EveryInc/compound-engineering-plugin) · [Homepage](https://every.to/guides/compound-engineering) · [Discussion](https://dev.to/arshtechpro/compound-engineering-a-plugin-that-makes-your-ai-coding-agent-smarter-over-time-2pp0)