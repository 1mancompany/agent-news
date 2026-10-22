---
title: "🔥 Hot Repo: The AI Bug-Hunter Cloudflare Runs on Its Own Code"
author: OMC Editorial
published_at: 2026-10-21T13:17:54.649978+00:00
slug: hot-repo-cloudflare-security-audit-skill
image: https://opengraph.githubassets.com/1/cloudflare/security-audit-skill
source: https://news.one-man-company.com/news/hot-repo-cloudflare-security-audit-skill
---

> **One-liner** — A coding-agent skill that coordinates isolated AI agents through a six-phase adversarial security audit, producing schema-validated, machine-readable findings — the same tool that seeded Cloudflare's internal vulnerability discovery harness.

- **Repo:** [cloudflare/security-audit-skill](https://github.com/cloudflare/security-audit-skill)
- **Stars:** ⭐ 35,155 (+1,997 today)
- **Language:** JavaScript / Markdown
- **License:** MIT

---

## What It Does

`security-audit-skill` turns any capable coding agent — Claude Code, Codex, Cursor — into a multi-phase security auditor. It orchestrates isolated agent instances through six sequential phases: reconnaissance, coverage-led vulnerability hunting per attack class, adversarial candidate validation, schema-validated structured output, independent record verification, and target-neutral reporting. Every confirmed finding requires a complete source trace; without one, it lands in `needs_validation`, not `confirmed`.

## Why It's Blowing Up

In June 2026, Cloudflare published ["Build your own vulnerability harness"](https://blog.cloudflare.com/build-your-own-vulnerability-harness/), revealing that this skill — originally ~450 lines — was the seed of a fleet-wide AI security system that can discover, validate, deduplicate findings, and open draft PRs across their entire codebase in roughly 14 hours. The open-source release was intentional: the README states it is "the skill that seeded Cloudflare's vulnerability discovery harness."

Today's +1,997 star spike — a 6% single-day jump at 35K stars — points to renewed attention, likely from a conference talk or follow-up coverage. The adversarial design is what's catching developers' eyes: the agent that validates a finding is never the agent that found it, which systematically eliminates a class of hallucination false positives that plague simpler "ask the model to review this code" approaches.

The skill also covers attack classes most AI code reviewers ignore: AI/LLM prompt injection, supply chain compromise, cloud misconfiguration, RPC/messaging tampering, and desktop/mobile IPC. Each class has its own specialized hunting file bundled with the skill.

## Key Features

- **Six-phase audit** — recon → hunt → validate → findings.json → record verification → report
- **Adversarial validation** — verifier agents are always fresh; hunters never self-verify
- **Additive repeat runs** — each run builds on prior ledgers to close coverage gaps rather than starting over
- **10 specialized attack classes** — memory safety, AI/LLM, web auth, supply chain, cloud, RPC, and more
- **Impact-based severity** — likelihood × impact, not checklist ticking; missing a secondary layer is a hardening note, not a vulnerability

## Quick Start

```bash
# Install the skill
npx skills add https://github.com/cloudflare/security-audit-skill --skill security-audit

# Then in Claude Code (or any supported agent), just ask:
# security audit this codebase
```

## The Verdict

If you run production code and want more than a linter pass, this is the most rigorous open-source security review workflow available for coding agents right now. The adversarial multi-agent architecture is a genuine architectural improvement over single-pass reviews, and the structured `findings.json` output makes it trivially scriptable into CI. The friction is real: you need Node.js, an agent with strong parallel tool use, and ideally a sandboxed environment to execute target code safely. A Haiku-tier run will underdeliver. But if you want to know what a patient adversary could realistically do to your codebase, and you're already on Claude Code, this is the first skill you should install.

📎 [GitHub](https://github.com/cloudflare/security-audit-skill) · [Cloudflare Blog](https://blog.cloudflare.com/build-your-own-vulnerability-harness/) · [Coverage at Remio.ai](https://www.remio.ai/post/cloudflare-security-audit-skill-turns-ai-code-review-into-an-adversarial-workflo)