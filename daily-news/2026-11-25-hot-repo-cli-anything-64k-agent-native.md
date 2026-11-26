---
title: "🔥 Hot Repo: 1,075 Stars in 24h — Agents Can Now Control Any GUI App"
author: OMC Editorial
published_at: 2026-11-25T13:12:08.694662+00:00
slug: hot-repo-cli-anything-64k-agent-native
image: https://opengraph.githubassets.com/1/HKUDS/CLI-Anything
source: https://news.one-man-company.com/news/hot-repo-cli-anything-64k-agent-native
---

> **One-liner** — CLI-Anything is a 7-phase pipeline and community registry that auto-generates agent-native CLI harnesses for any software, letting AI agents control apps like Blender, LibreOffice, and GIMP via structured JSON — no screenshots, no GUI scraping.

- **Repo:** [HKUDS/CLI-Anything](https://github.com/HKUDS/CLI-Anything)
- **Stars:** ⭐ ~64,400 (+1,075 today)
- **Language:** Python
- **License:** Apache 2.0

---

## What It Does

CLI-Anything converts GUI and desktop applications into command-line interfaces that AI agents can call with structured JSON output. It ships as both a Claude Code plugin and a pip package. A 7-phase generator pipeline — analyze, design, implement, plan tests, write tests, document, publish — takes a path to any software directory and produces a fully-tested, documented CLI harness complete with `--json` flags, REPL mode, and a SKILL.md that agents read to discover available commands.

## Why It's Blowing Up

The core bottleneck for agentic workflows in 2026 is **the last mile**: AI coding agents handle text files and terminals fine, but apps like Blender, LibreOffice, and GIMP have no machine-readable API surface. Screenshot-based computer use is brittle at scale. CLI-Anything's answer is to generate a thin, stable CLI wrapper that calls the real backend rather than reimplementing it — a LibreOffice harness calls LibreOffice headless, a Blender harness calls Blender's Python API.

The HKU Data Science Lab backed the release with an arXiv paper (2606.03854), giving it academic credibility rare in tooling repos. Meanwhile, **CLI-Hub**, the community registry bundled with the project, already lists 40+ ready-made harnesses across creative, office, data, GIS, and AI service categories. Agents install any of them in one command and get structured access to complex software without a line of wrapper code.

The timing is sharp: every major coding agent — Claude Code, Cursor, Codex, Hermes — shipped plugin and skill ecosystems this year. CLI-Anything slots directly into all of them from day one, and the project has accumulated over 2,460 passing tests to back its stability claims.

## Key Features

- **7-phase generator** — Analyze → Design → Implement → Test → Document → Publish, fully automated from a directory path
- **CLI-Hub registry** — Browse, install, update 40+ community-built harnesses with `cli-hub install <name>`
- **Structured JSON output** — Every generated CLI supports `--json` flag and REPL mode for deterministic agent loops
- **SKILL.md auto-generation** — Each harness ships a machine-readable skill definition agents discover automatically
- **Broad platform support** — Claude Code, Cursor, Codex, OpenClaw, Hermes, GitHub Copilot CLI, and more

## Quick Start

```bash
# Install the CLI-Hub package manager
pip install cli-anything-hub

# Install a pre-built harness (e.g. LibreOffice)
cli-hub install libreoffice

# Or generate a harness from source inside Claude Code
/plugin marketplace add HKUDS/CLI-Anything
/cli-anything ./my-app
```

## The Verdict

CLI-Anything is essential if you're building agents that need to operate complex desktop software — creative tools, office suites, or domain-specific apps with no REST API. It is not lightweight: generating a harness for a large app takes dozens of agent turns and several `/refine` cycles, and the project honestly requires frontier-tier models to work well. But for teams running production agents that need to touch more than a filesystem, this is the most principled open-source solution currently available. Worth starring if you're betting on agents in 2026.

📎 [GitHub](https://github.com/HKUDS/CLI-Anything) · [CLI-Hub](https://pypi.org/project/cli-anything-hub/) · [Paper](https://arxiv.org/abs/2606.03854)