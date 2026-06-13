---
title: "🔥 Hot Repo: 1-in-4 AI Agent Skills Are Backdoored — NVIDIA Fixed It"
author: OMC Editorial
published_at: 2026-06-12T13:11:32.158351+00:00
slug: hot-repo-nvidia-skillspector
image: https://opengraph.githubassets.com/1/NVIDIA/SkillSpector
source: https://news.one-man-company.com/news/hot-repo-nvidia-skillspector
---

> **One-liner** — SkillSpector is NVIDIA's open-source security scanner that audits AI agent skills for vulnerabilities, malicious patterns, and backdoors before you install them.

- **Repo:** [NVIDIA/SkillSpector](https://github.com/NVIDIA/SkillSpector)
- **Stars:** ⭐ 3,111 (+811 today)
- **Language:** Python
- **License:** Apache 2.0

---

## What It Does

SkillSpector runs a two-stage analysis on any AI agent skill: first, a fast static pass using AST analysis and pattern matching against 64 vulnerability templates across 16 categories; then an optional LLM-powered semantic sweep to filter false positives and explain findings in plain English. It accepts Git repos, URLs, ZIP archives, directories, or single files, and outputs risk scores from 0–100 with explicit install/reject recommendations.

## Why It's Blowing Up

The AI agent skill marketplace has exploded — Claude Code, OpenClaw, Cursor, and a dozen other platforms now host thousands of community-built skills that drop into any developer's agent with a single command. The problem: NVIDIA's own research found **26.1% of skills contain exploitable vulnerabilities**, and **5.2% show likely malicious intent**. Snyk's parallel ToxicSkills study, scanning 3,984 skills on ClawHub, found 76 confirmed credential-stealing or backdoor payloads hiding behind normal-looking skill descriptions.

NVIDIA shipped SkillSpector on May 22, 2026, alongside its Verified Agent Skills program — a catalog of 162 cryptographically signed skills, each passing a SkillSpector scan before publication. The timing is sharp: as skill marketplaces race for developer adoption, nobody was auditing the supply chain. SkillSpector fills that gap, and its jump to 3k+ stars in under three weeks shows the community already knows it.

## Key Features

- **Two-stage analysis** — fast static AST scanning followed by optional LLM semantic evaluation for accuracy
- **64 vulnerability patterns** — 16 categories covering prompt injection, MCP tool poisoning, privilege escalation, and data exfiltration
- **Live CVE lookups** — real-time dependency vulnerability checks via OSV.dev with offline fallback
- **SARIF output** — native integration with GitHub Advanced Security and standard CI/CD pipelines
- **Multi-format input** — scans Git repos, URLs, ZIP files, directories, or single Markdown/Python files

## Quick Start

```bash
git clone https://github.com/NVIDIA/skillspector.git
cd skillspector
uv venv .venv && source .venv/bin/activate && make install
skillspector scan https://github.com/user/my-agent-skill
```

## The Verdict

If you're installing third-party skills into Claude Code, OpenClaw, or any MCP-compatible agent — and most teams are — SkillSpector belongs in your pre-install checklist. The 26% vulnerability rate isn't FUD; it's NVIDIA's own research, independently corroborated by Snyk. The tool is fast enough to run in CI, flexible enough to scan anything from a GitHub URL to a local zip, and backed by a team maintaining a live verified skill catalog. Skip it if your entire agent toolchain is in-house. Otherwise, star it and add it to your pipeline today.

📎 [GitHub](https://github.com/NVIDIA/SkillSpector) · [NVIDIA Blog](https://developer.nvidia.com/blog/nvidia-verified-agent-skills-provide-capability-governance-for-ai-agents/) · [Docs](https://docs.nvidia.com/skills/scanning-agent-skills)
