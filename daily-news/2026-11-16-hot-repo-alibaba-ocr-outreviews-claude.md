---
title: "🔥 Hot Repo: Alibaba's Secret Weapon Now Outreviews Claude Code"
author: OMC Editorial
published_at: 2026-11-16T13:12:34.492031+00:00
slug: hot-repo-alibaba-ocr-outreviews-claude
image: https://raw.githubusercontent.com/alibaba/open-code-review/main/imgs/highlights-en.png
source: https://news.one-man-company.com/news/hot-repo-alibaba-ocr-outreviews-claude
---

> **One-liner** — OpenCodeReview is Alibaba's battle-tested AI code review CLI that pairs a deterministic engineering pipeline with an LLM agent to deliver precise, line-level review comments at 1/9th the token cost of general-purpose agents.

- **Repo:** [alibaba/open-code-review](https://github.com/alibaba/open-code-review)
- **Stars:** ⭐ ~51,700 (+688 today)
- **Language:** Go
- **License:** Apache-2.0

---

## What It Does

OpenCodeReview (`ocr`) is a CLI tool that reads Git diffs, routes changed files through deterministic selection and rule-matching logic, then hands the result to an LLM agent that produces structured, line-level review comments. Unlike general-purpose coding agents, the architecture uses engineering logic — not the model — for the steps where accuracy is non-negotiable: file selection, bundling, rule matching, and comment positioning.

## Why It's Blowing Up

Alibaba originally built this tool for internal use and ran it across tens of thousands of engineers for two years, reportedly identifying millions of code defects, before releasing it publicly in May 2026. That pedigree is rare in open source: most projects publish first and validate later.

Version 1.13.10 dropped on November 15, 2026, capping a release cadence that went from v1.9.7 to v1.13.10 in under three months. Alibaba backs the tool with the AACR-Bench benchmark — 50 real-world repos, 200 pull requests, 10 languages, annotated by 80+ senior engineers — showing OCR outperforms Claude Code on both precision and F1 with the same underlying model while using ~1/9th the tokens. The trade-off is lower recall, which the team frames as a deliberate feature: fewer false alarms is more useful in a high-volume CI pipeline.

The support matrix has become a draw in its own right. It integrates with Claude Code, Codex, Cursor, Kimi Code, and OpenCode, and offers a delegation mode where your existing coding agent runs the review using its own credentials — no extra API key required.

## Key Features

- **Delegation Mode** — your existing coding agent (Claude Code, Codex, Cursor) runs the review with its own model, no OCR API key needed
- **MCP Server** — exposes OCR as an MCP tool so agents can call it directly from within their own context
- **`ocr scan`** — full-file audit mode that works without any git diff, useful for onboarding an unfamiliar codebase
- **Multi-language ruleset** — built-in rules for NPE, thread-safety, XSS, and SQL injection across 10+ programming languages

## Quick Start

```bash
npm install -g @alibaba-group/open-code-review
ocr config provider   # pick Anthropic, OpenAI, DeepSeek, or custom
ocr review            # review all staged and unstaged changes
```

## The Verdict

If your team uses Claude Code for code review today and wants faster, cheaper, more precise feedback on large PRs, `ocr` is worth a serious look. The 1/9th token claim is Alibaba's own benchmark, but the architecture — deterministic file selection, rule-matching, and positioning outside the LLM — is sound engineering that explains why the numbers could hold up. It's not for teams who want high recall and are fine sifting through noise; it's tuned toward precision. For CI pipelines where false alarms carry a real cost, this is now the strongest open-source option in the category.

📎 [GitHub](https://github.com/alibaba/open-code-review) · [Docs](https://open-codereview.ai/docs) · [Benchmark](https://huggingface.co/datasets/Alibaba-Aone/aacr-bench) · [npm](https://www.npmjs.com/package/@alibaba-group/open-code-review)