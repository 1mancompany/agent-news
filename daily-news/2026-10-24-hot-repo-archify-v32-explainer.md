---
title: "🔥 Hot Repo: 88K Stars — Diagrams That Actually Explain Themselves"
author: OMC Editorial
published_at: 2026-10-24T13:11:24.886023+00:00
slug: hot-repo-archify-v32-explainer
image: https://opengraph.githubassets.com/1/tt-a1i/archify
source: https://news.one-man-company.com/news/hot-repo-archify-v32-explainer
---

> **One-liner** — Archify is a Claude Code / Codex agent skill that converts any codebase, idea, or question into an interactive HTML diagram, now with one-page explainers in v3.2.0.

- **Repo:** [tt-a1i/archify](https://github.com/tt-a1i/archify)
- **Stars:** ⭐ 88,546
- **Language:** JavaScript
- **License:** MIT

---

## What It Does

Archify is an agent skill that lets Claude Code, Codex CLI, Cursor, and OpenCode turn natural-language descriptions into self-contained interactive HTML files. The output is not a static PNG — nodes are clickable, paths are traceable, and themes switch between light and dark. It supports 10 diagram types: architecture, workflow, sequence, dataflow, lifecycle, ERD, class/interface, tree, timeline, and waterfall.

## Why It's Blowing Up

The v3.2.0 release on October 18 introduced **one-page explainers** — a format where your agent produces a publication-quality HTML page organized around a question. Each panel answers one sub-question, interleaving prose, tables, code blocks, and native diagrams. Steps sit beside the diagram they walk through and highlight nodes as you read. The finished page exports to PNG, WebP, JPG, or PDF in four visual styles.

Two weeks before that, v3.1.0 doubled the number of supported diagram types from five to ten, adding ERD, class, tree, timeline, and waterfall. Combined, the two releases represent the biggest expansion in the project's history, and the activity is showing: 130K+ installs are tracked on skills.sh with 88K GitHub stars.

The unlock is the no-repository requirement. You can start from a plain description ("Browser calls the API, the API checks Redis, cache miss queries Postgres"), and the skill generates a verified, versioned diagram. For teams using Claude Code in long-running agent sessions, this fills a real gap: producing shareable visual artifacts without leaving the terminal.

## Key Features

- **10 diagram types** — architecture, workflow, sequence, dataflow, lifecycle, ERD, class, tree, timeline, waterfall
- **One-page explainers** — ask a question, get a multi-panel interactive HTML page with diagrams, citations, and steps
- **Source evidence** — repository excerpts are pinned to a commit SHA and linked inline in each panel
- **Export everywhere** — standalone HTML, PNG, WebP, JPG long image, or PDF across four visual styles

## Quick Start

```bash
npx skills add tt-a1i/archify -g
```

Then tell your agent:

```
Use Archify to answer as one page: our API P99 went from 80ms to 600ms 
while the mean barely moved. What is the likely cause and how do we investigate?
```

## The Verdict

If you use Claude Code or Codex regularly and find yourself screenshotting terminal output to share with teammates, install this now. It does one thing — turning agent work into shareable visual artifacts — and does it well enough that 130K developers are running it without a significant viral moment. The v3.2.0 explainer format is the standout new capability: it's a genuine replacement for ADRs and incident write-ups when you want diagrams embedded in the narrative. It is not for teams that maintain diagrams manually in Lucidchart or Miro; it excels when the diagram is generated on demand and discarded or versioned as code.

📎 [GitHub](https://github.com/tt-a1i/archify) · [Website](https://archify.si) · [Gallery](https://archify.si/gallery.html)
