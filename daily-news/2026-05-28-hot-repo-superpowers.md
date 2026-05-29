---
title: "🔥 Hot Repo: 210K Stars — Forces Claude to Delete Untested Code"
author: OMC Editorial
published_at: 2026-05-28T13:15:25.42668+00:00
slug: hot-repo-superpowers
image: https://opengraph.githubassets.com/1/obra/superpowers
source: https://news.one-man-company.com/news/hot-repo-superpowers
---

> **One-liner** — obra/superpowers is a skills framework that injects a complete software development methodology — spec, plan, TDD, subagent execution, code review — into Claude Code and seven other coding agents.

- **Repo:** [obra/superpowers](https://github.com/obra/superpowers)
- **Stars:** ⭐ 210,586 (+trending today on GitHub daily)
- **Language:** Shell
- **License:** MIT License

---

## What It Does

Superpowers installs a set of composable Markdown skill files into your coding agent that automatically activate at the right moment in your workflow. When you ask Claude Code to build something, the agent doesn't jump into code — it runs a structured 7-phase sequence: brainstorm a spec (reviewed in chunks), set up a git worktree, write an implementation plan broken into 2–5 minute tasks, dispatch fresh subagents per task with two-stage review, enforce TDD with a rule that deletes code written before tests exist, and present merge or PR options at the end. The same skill folder works identically across Claude Code, Codex CLI, Codex App, Cursor, Gemini CLI, OpenCode, GitHub Copilot CLI, and Factory Droid.

## Why It's Blowing Up

Jesse Vincent published Superpowers on October 9, 2025 — the same day Anthropic launched the Claude Code plugin system — and it found product-market fit immediately. By January 2026 it had 30K stars; by March, 94K; by April, 150K; today it sits at 210K, making it one of the fastest-growing open-source projects of the year and a daily-trending fixture on GitHub.

The timing is deliberate. Claude Code shipped increasingly powerful autonomous capabilities, but powerful ≠ disciplined: agents jumped straight to code, skipped tests, and produced demos that collapsed under real engineering review. Superpowers is the antidote. It replaces improvisation with a software development culture encoded in Markdown — every session gets a spec you review in chunks, an implementation plan you sign off on, and a TDD cycle that will literally delete code written before a failing test is in place.

In early 2026, Anthropic added Superpowers to its official Claude plugin marketplace, giving it the equivalent of an App Store Editor's Choice badge. The v5.1.0 release (May 4, 2026) pruned legacy slash commands and removed a redundant named agent, folding everything into the leaner skill-dispatch model that works across all eight supported harnesses.

## Key Features

- **7-Phase Enforced Workflow** — Brainstorm → Spec → Worktree → Plan → Subagent Dev → Review → Finish; each phase activates automatically
- **TDD Enforcer** — strict RED-GREEN-REFACTOR; code written before a failing test exists is deleted by the agent
- **Subagent-Driven Development** — dispatches a fresh subagent per task with two-stage review (spec compliance, then code quality)
- **Multi-Harness Support** — the same skill folder works across 8 agents: Claude Code, Codex CLI/App, Cursor, Gemini CLI, OpenCode, Copilot CLI, Factory Droid
- **Git Worktree Integration** — every feature gets an isolated branch and clean workspace from the first commit

## Quick Start

```bash
# Claude Code — via official Anthropic marketplace
/plugin install superpowers@claude-plugins-official

# Or register the Superpowers marketplace first
/plugin marketplace add obra/superpowers-marketplace
/plugin install superpowers@superpowers-marketplace
```

## The Verdict

Superpowers is for developers who've been burned by Claude producing "working" code that collapses under engineering review — and who want structure, not just smarts, from their agent. If you regularly build features that need real tests, real planning, and peer review before merge, this plugin pays for itself in the first session. It's not for vibe-coders who want fast and loose iteration; the mandatory spec and planning phases add 5–10 minutes of upfront friction per feature. At 210K stars and on Anthropic's official marketplace after only seven months, it's the closest thing the Claude Code ecosystem has to a standard engineering playbook.

📎 [GitHub](https://github.com/obra/superpowers) · [Marketplace](https://claude.com/plugins/superpowers) · [Community Discord](https://discord.gg/35wsABTejz) · [Prime Radiant](https://primeradiant.com)
