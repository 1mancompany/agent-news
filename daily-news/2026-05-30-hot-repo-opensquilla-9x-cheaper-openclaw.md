---
title: "🔥 Hot Repo: 9x Cheaper Than OpenClaw, Same Benchmark"
author: OMC Editorial
published_at: 2026-05-30T13:10:53.725116+00:00
slug: hot-repo-opensquilla-9x-cheaper-openclaw
image: https://opengraph.githubassets.com/1/opensquilla/opensquilla
source: https://news.one-man-company.com/news/hot-repo-opensquilla-9x-cheaper-openclaw
---

> **One-liner** — OpenSquilla is a microkernel AI agent that routes every turn to the cheapest capable model using an on-device ML classifier, hitting near-identical task scores to OpenClaw at 9x lower cost.

- **Repo:** [opensquilla/opensquilla](https://github.com/opensquilla/opensquilla)
- **Stars:** ⭐ 2,115 (+~25 today)
- **Language:** Python
- **License:** Apache-2.0

---

## What It Does

OpenSquilla is an open-source AI agent for CLI, Web UI, and 10+ messaging platforms (Telegram, Discord, Slack, Feishu, Matrix). Its standout feature is **SquillaRouter** — an on-device LightGBM + ONNX classifier that scores each turn's complexity using length, language, code patterns, and semantic embeddings, then routes it to one of four model tiers (T0–T3). Cheap turns hit budget models; complex turns escalate to frontier ones. The routing decision runs locally — your prompt never leaves the machine to decide which model handles it.

## Why It's Blowing Up

The benchmark data is driving the attention. Against PinchBench 1.2.1 (25 real-world tasks), OpenSquilla scored 0.9251 with a mixed-model routing setup versus OpenClaw's 0.9255 on Claude Opus 4.7 alone. Scores are statistically indistinguishable. The cost is not: OpenClaw spent $6.23; OpenSquilla spent $0.69 — 9x cheaper on an identical workload.

Token consumption tracked the same pattern — 1.7M input tokens versus OpenClaw's 3M, a 44% reduction — because SquillaRouter also scales the system prompt with task complexity, stripping full instructions down to lightweight variants for trivial turns.

The v0.2.0 release (May 19) added a further pull: one-command migration from OpenClaw and Hermes Agent configs, including memory, personas, skills, and MCP settings. That targets the large installed base of both competing agents and makes it trivial to run a side-by-side cost comparison before switching.

## Key Features

- **SquillaRouter** — local ML classifier routes turns across four model tiers; routing decision runs fully on-device
- **20+ LLM providers** — OpenRouter, OpenAI, Anthropic, Ollama, DeepSeek, Gemini, Groq, Mistral, vLLM, and more with primary-plus-fallback
- **MCP client and server** — acts as both sides of the Model Context Protocol via `opensquilla mcp-server run`
- **Layered security sandbox** — three policy tiers with Bubblewrap on Linux; denial ledger pauses autonomous runs after repeated failures

## Quick Start

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh && . "$HOME/.local/bin/env"
uv tool install --python 3.12 "opensquilla[recommended] @ https://github.com/opensquilla/opensquilla/releases/download/v0.2.1/opensquilla-0.2.1-py3-none-any.whl"
opensquilla onboard && opensquilla gateway run
```

## The Verdict

If you run AI agents in production and pay frontier-model rates on every turn, OpenSquilla is worth a serious look. The PinchBench numbers are a legitimate argument: a 9x cost delta across 25 real tasks is not a toy benchmark. The caveat is that SquillaRouter's routing quality will vary with your specific workload — tasks outside PinchBench's corpus may not see the same savings, and the feature set is still maturing (sandbox on macOS and Windows is incomplete, several runtime features are in-progress). Not for teams needing a battle-tested single-model setup. Absolutely worth starring if token bills are already a line item you manage.

📎 [GitHub](https://github.com/opensquilla/opensquilla) · [Homepage](https://opensquilla.ai) · [Discussion](https://github.com/opensquilla/opensquilla/issues)
