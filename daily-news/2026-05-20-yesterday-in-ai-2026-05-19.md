---
title: "Yesterday in AI: 19 May 2026 — Google Bets Everything on Agents at I/O"
author: OMC Editorial
published_at: 2026-05-20T08:13:09.466582+00:00
slug: yesterday-in-ai-2026-05-19
image: https://images.unsplash.com/photo-1677442135703-1787eea5ce01?w=1200&q=80
source: https://news.one-man-company.com/news/yesterday-in-ai-2026-05-19
---

> **TL;DR** — Google launched Gemini 3.5 Flash at I/O 2026, a Flash-tier model running at 289 tokens/sec (4x frontier peers) that now beats Gemini 3.1 Pro on coding and agent benchmarks; Anthropic shipped MCP tunnels and self-hosted sandboxes for Claude Managed Agents, enabling private-network tool access with zero inbound firewall rules; Anthropic lifted confidentiality on Claude Mythos, letting 50+ Project Glasswing partners openly share findings about its autonomous zero-day-hunting capabilities.

---

## 1️⃣ Google I/O 2026: Flash-Tier Model Beats Pro on Every Agent Benchmark

- **What:** Google launched Gemini 3.5 Flash at I/O 2026 — an agentic model that surpasses Gemini 3.1 Pro on coding and agent benchmarks at Flash speed and price.
- **Why it matters:** For the first time a Flash-tier model beats the Pro tier, flipping Google's model hierarchy and signaling that agents, not chatbots, are now the primary design target.
- **Key number:** 289 tokens/sec — 4x faster than other frontier models — at $1.50/$9.00 per million input/output tokens, 40% cheaper than Gemini 3.1 Pro.

Gemini 3.5 Flash ships with a 1-million-token context window, dynamic thinking on by default (auto-allocating extra compute for harder problems), and multimodal inputs (text, image, audio, video). On agentic benchmarks it scores 76.2% on Terminal-Bench 2.1 and 83.6% on MCP Atlas — both above 3.1 Pro. Google says the model independently built an operating system from scratch in internal tests without human intervention.

The model is live via the Gemini API, Antigravity (Google's agent-first dev platform), and Gemini Enterprise. Google also announced Gemini Spark — a general-purpose AI agent reasoning across connected apps — in beta for AI Ultra subscribers next week, and Co-Scientist, a Gemini-powered research acceleration tool for scientific workflows. Gemini Omni, a multimodal creation model, was also previewed.

📎 [CNBC](https://www.cnbc.com/2026/05/19/google-ai-ultra-gemini-spark-omni.html) · [TechCrunch](https://techcrunch.com/2026/05/19/with-gemini-3-5-flash-google-bets-its-next-ai-wave-on-agents-not-chatbots/) · [MarkTechPost](https://www.marktechpost.com/2026/05/20/google-introduces-gemini-3-5-flash-at-i-o-2026-a-faster-and-cheaper-model-for-ai-agents-and-coding/)

---

## 2️⃣ Anthropic Ships MCP Tunnels and Self-Hosted Sandboxes for Claude Agents

- **What:** Anthropic added two enterprise features to Claude Managed Agents at its Code with Claude London event: MCP tunnels (research preview) and self-hosted sandboxes (public beta).
- **Why it matters:** Enterprises can now connect Claude agents to private internal systems without exposing any endpoints to the public internet — removing a key adoption blocker in regulated industries.
- **Key number:** Zero inbound firewall rules required — MCP tunnels use a single outbound connection with end-to-end encryption.

MCP tunnels let Claude Managed Agents call MCP servers inside a private network — internal databases, APIs, knowledge bases, ticketing systems — without opening public endpoints. A lightweight gateway initiates one outbound connection; all traffic is encrypted. For self-hosted sandboxes, tool execution moves to customer-controlled infrastructure (supported providers: Cloudflare, Daytona, Modal, Vercel) while the agent orchestration loop stays on Anthropic's side.

Self-hosted sandboxes are particularly valuable for compute-heavy agentic workloads — long CI builds, image generation, or tasks requiring resources beyond Anthropic's defaults. Both features target the compliance and data-residency requirements that have slowed agentic deployments in finance, healthcare, and government.

📎 [9to5Mac](https://9to5mac.com/2026/05/19/anthropic-enhances-claude-managed-agents-with-two-new-privacy-and-security-features/) · [The Decoder](https://the-decoder.com/anthropic-adds-self-hosted-sandboxes-and-mcp-tunnels-to-claude-managed-agents/) · [InfoQ](https://www.infoq.com/news/2026/05/claude-mcp-tunnels/)

---

## 3️⃣ Anthropic Lifts Claude Mythos Secrecy as Zero-Day Count Grows

- **What:** Anthropic removed confidentiality requirements for Project Glasswing participants, allowing ~50 partner organizations — including AWS, Apple, Microsoft, and Google — to openly share Claude Mythos findings.
- **Why it matters:** Mythos has autonomously discovered thousands of zero-days across every major OS and browser; open disclosure accelerates defensive patching before the capabilities become more widely understood.
- **Key number:** 4 independent bugs chained by Mythos into a single exploit that bypassed both browser renderer and OS sandboxing simultaneously — with no human involvement.

Claude Mythos Preview had operated under strict NDAs since its restricted launch within Project Glasswing. Demonstrations to date include independently exploiting a 17-year-old remote code execution vulnerability in FreeBSD's NFS server (discovery, exploitation, and a 20-gadget ROP chain distributed across packets — fully autonomous) and local privilege escalation in Linux via race condition vulnerabilities. The model's capacity to discover and chain vulnerabilities at scale is what originally prompted the confidentiality requirement.

Anthropic says it has no plans to make Mythos generally available while it develops cybersecurity safeguards. The shift to open sharing is likely designed to surface defensive patches faster through coordinated disclosure — keeping findings siloed while the vulnerability surface is this large carries its own risk.

📎 [Gizmodo](https://gizmodo.com/anthropic-is-loosening-the-secrecy-around-claude-mythos-so-findings-can-be-shared-broadly-2000760355) · [Anthropic Red Team](https://red.anthropic.com/2026/mythos-preview/) · [Schneier on Security](https://www.schneier.com/blog/archives/2026/04/on-anthropics-mythos-preview-and-project-glasswing.html)