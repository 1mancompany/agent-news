---
title: "🔥 Hot Repo: 36K Devs Turned Claude Code Into a 5-Agent Team"
author: OMC Editorial
published_at: 2026-06-14T13:14:59.37098+00:00
slug: hot-repo-oh-my-claudecode-teams
image: https://opengraph.githubassets.com/1/Yeachan-Heo/oh-my-claudecode
source: https://news.one-man-company.com/news/hot-repo-oh-my-claudecode-teams
---

> **One-liner** — oh-my-claudecode is an open-source orchestration plugin for Claude Code that turns a single session into a coordinated team of up to 5 parallel AI agents, routing subtasks to Claude, Codex, Gemini, or Grok workers with zero configuration.

- **Repo:** [Yeachan-Heo/oh-my-claudecode](https://github.com/Yeachan-Heo/oh-my-claudecode)
- **Stars:** ⭐ 36,360 (v4.14.7 released today)
- **Language:** TypeScript
- **License:** MIT

---

## What It Does

oh-my-claudecode (OMC) plugs directly into Claude Code as a marketplace plugin or npm package, adding 19 specialized agent roles (architect, coder, reviewer, tester, researcher) and 39 built-in skills. Its core primitive is the `/team` command, which stages a task through a plan → PRD → execute → verify pipeline across multiple parallel workers. Workers can be Claude, Codex, Gemini, or Grok CLI panes — each running in a separate tmux window, spawned on demand and killed when their task completes.

## Why It's Blowing Up

Today's v4.14.7 release added Claude Fable 5 model tier support — the first update to officially recognize Anthropic's newest flagship — and shipped Cursor provider integration alongside team-launch stability fixes. Developers evaluating Fable 5 for coding workloads now have a one-stop upgrade path inside the tool they're already using.

OMC hit 36k stars in roughly five months (created January 2026), powered by a team mode that solves a real friction point: Claude Code's built-in experimental team support (`CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS=1`) only routes tasks to Claude, while OMC lets one command fan out to Codex for security review and Gemini for UI critique simultaneously. The reported 3–5× throughput improvement and 30–50% cost reduction on parallelisable workloads are the numbers circulating in the project's Discord (6,000+ members).

The project ships more than 100 PRs per month and its changelog has become a reliable signal for what Claude Code power-users actually care about — this release alone touched 11 bug fixes and 2 new features in a single patch.

## Key Features

- **19 specialized agents** — architect, coder, reviewer, tester, researcher ship out of the box, each with scoped tool permissions
- **Cross-model team workers** — `omc team 2:codex` / `2:gemini` / `2:grok` spawn real tmux worker panes alongside Claude
- **39 built-in skills** — TDD, code review, refactoring, deployment, `/deep-interview` for Socratic requirement clarity before any code is written
- **Claude Fable 5 routing** — today's v4.14.7 adds the `fable-5` tier alias and model ID so agents can target Anthropic's latest model explicitly

## Quick Start

```bash
# Install via Claude Code marketplace (recommended)
/plugin marketplace add https://github.com/Yeachan-Heo/oh-my-claudecode
/plugin install oh-my-claudecode

# Or via npm
npm i -g oh-my-claude-sisyphus@latest

# Run a 3-agent parallel task inside Claude Code
/team 3:executor "fix all TypeScript errors in src/"

# Kick off a fully autonomous build
/autopilot "build a REST API for managing tasks"
```

## The Verdict

If you're already in Claude Code daily and hitting the single-thread ceiling on complex projects — parallel code review, multi-module refactors, build-test-fix loops — OMC is the most mature open-source answer at 36k stars and a release cadence that tracks Anthropic's model updates in real time. Today's Fable 5 support lands on day one of the model's wider availability, which tells you something about how closely the maintainers track upstream. Skip it if your workflow is simple and sequential; the tmux-based multi-agent runtime assumes terminal fluency and the slash-command surface takes an afternoon to learn. For everyone else, this is the upgrade Claude Code ships without.

📎 [GitHub](https://github.com/Yeachan-Heo/oh-my-claudecode) · [Docs](https://yeachan-heo.github.io/oh-my-claudecode-website) · [Discord](https://discord.gg/sj4exxQ9v)
