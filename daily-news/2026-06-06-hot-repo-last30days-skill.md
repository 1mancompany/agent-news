---
title: "🔥 Hot Repo: The Agent That Searches Reddit, X & Polymarket — Not Google"
author: OMC Editorial
published_at: 2026-06-06T13:07:54.000189+00:00
slug: hot-repo-last30days-skill
image: https://opengraph.githubassets.com/1/mvanhorn/last30days-skill
source: https://news.one-man-company.com/news/hot-repo-last30days-skill
---

> **One-liner** — `/last30days` is a Claude Code skill that fans out across Reddit, X, YouTube, TikTok, Hacker News, and Polymarket simultaneously, scoring results by actual human engagement instead of editorial curation.

- **Repo:** [mvanhorn/last30days-skill](https://github.com/mvanhorn/last30days-skill)
- **Stars:** ⭐ 28,400 (+731 today)
- **Language:** Python
- **License:** MIT

---

## What It Does

`/last30days` is an AI agent skill that plugs into Claude Code, Codex, Cursor, GitHub Copilot CLI, and 50+ other agent hosts, then fans out searches across a dozen social platforms in parallel: Reddit, X, YouTube, TikTok, Hacker News, Polymarket, GitHub, and more. Instead of editorial ranking, it scores results by what people actually engaged with — Reddit upvotes, X likes, YouTube view counts, and real-money Polymarket odds. Every synthesized brief attributes each claim to a specific source with a citation.

## Why It's Blowing Up

The project hit GitHub Trending #1 today with +731 stars, fueled by v3's intelligent entity resolution: type `OpenClaw` and the engine pre-resolves the creator's X handle, relevant subreddits, and YouTube channels before the first API call fires. The old approach matched keywords; v3 understands the topic first, then searches the right people and communities.

The deeper unlock is bridging platform silos that no single AI can cross natively. Google can't touch Reddit comments. ChatGPT has a Reddit deal but no X access. Gemini has YouTube but not Reddit. `/last30days` lets you bring your own API keys and bridge all of them through a single agent command. The motto — "Google aggregates editors. /last30days searches people." — has been spreading in dev circles and landing on Hacker News.

Polymarket integration is the differentiator no web search offers: prediction market odds backed by real money. A query on a product acquisition surfaces not just opinions but "68% acquired by Q3" — a harder signal than any analyst report.

## Key Features

- **Multi-platform parallel search** — Reddit, X, YouTube, TikTok, HN, Polymarket, GitHub searched simultaneously
- **Entity resolution (v3)** — Pre-research phase resolves handles, subreddits, and hashtags before the first query fires
- **Engagement-weighted ranking** — Scores by upvotes, likes, view counts, and Polymarket odds — not SEO rank
- **Shareable HTML briefs** — `--emit=html` exports a self-contained dark-mode file ready for Slack or email
- **Cross-source cluster merging** — Same story on Reddit, X, and YouTube is merged into one entry
- **Zero config to start** — Reddit, HN, Polymarket, and GitHub work immediately; a setup wizard unlocks the rest

## Quick Start

```bash
# Claude Code (auto-updates via marketplace)
/plugin marketplace add mvanhorn/last30days-skill
/plugin install last30days

# Codex, Cursor, Copilot, Gemini CLI
npx skills add mvanhorn/last30days-skill -g

# Run it
/last30days Anthropic Claude 4
/last30days "OpenAI vs Anthropic" --emit=html
```

## The Verdict

If you do research before meetings, competitive analysis, or keeping up with fast-moving AI trends, this is genuinely useful. The Polymarket integration alone separates it from every other research tool — you get financially-incentivized signals alongside social consensus. It's not right for factual lookups where a basic web search is faster. But for "what is the developer community actually saying about X right now" — nothing else comes close. Try `/last30days` on your own company name and prepare to be surprised.

📎 [GitHub](https://github.com/mvanhorn/last30days-skill) · [Agent Skills Registry](https://agentskills.io) · [Changelog](https://github.com/mvanhorn/last30days-skill/blob/main/CHANGELOG.md)