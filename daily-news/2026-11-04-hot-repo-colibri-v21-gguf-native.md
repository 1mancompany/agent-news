---
title: "🔥 Hot Repo: Native GGUF, Zero Python — 1T Models Run Locally"
author: OMC Editorial
published_at: 2026-11-04T13:19:13.256516+00:00
slug: hot-repo-colibri-v21-gguf-native
image: https://opengraph.githubassets.com/1/JustVugg/colibri
source: https://news.one-man-company.com/news/hot-repo-colibri-v21-gguf-native
---

> **One-liner** — Colibri is a pure C inference engine that streams mixture-of-experts model experts from disk so frontier models from 35B to 1 trillion parameters run on hardware you already own — no Python, no cloud, no dependencies.

- **Repo:** [JustVugg/colibri](https://github.com/JustVugg/colibri)
- **Stars:** ⭐ ~47,000 (trending today following v2.1.0)
- **Language:** C
- **License:** Apache-2.0

---

## What It Does

Colibri is a self-contained C inference engine that runs large MoE models by loading only the expert layers each token actually routes to, keeping memory usage far below the full model weight. A model with 744 billion or more parameters that would normally require a cluster runs on a consumer machine because only a fraction of the total weights are ever in memory simultaneously. No Python runtime, no package manager, no cloud account — it unpacks, builds with `make`, and runs.

## Why It's Blowing Up

v2.1.0 landed on October 31, and it crossed two lines that change Colibri from a curiosity to a credible inference platform.

The first is native GGUF support. Before v2.1.0, you had to use Colibri's own model format, which meant converting files or downloading from the project's own Hugging Face organization. Now `coli import model.gguf` accepts any GGUF without conversion or re-quantization. That unlocks every quantized model on Hugging Face — tens of thousands of files — for use in Colibri with one command.

The second is cross-platform GPU acceleration. v2.1.0 ships a Linux and Windows Vulkan backend where models larger than VRAM overflow experts into a RAM pool, a Windows CUDA archive for NVIDIA cards (compute 8.0+), and an Apple Silicon macOS build with Metal. For the first time, users on NVIDIA, AMD, and Apple Silicon all have accelerated paths without compiling from source.

New model support adds Mistral-Large-4 — 1 trillion total parameters, 52B active via MoE — plus Muse Spark Open (816B), DeepSeek V4.1 Flash GGUFs, and Qwen3.8-Flash-Next at 262,144-token context. The KV cache switched to float16, roughly halving RAM use; GLM-5.3 at a 131K context drops from 23.9 GB to 11.9 GB resident. The release draws from 387 pull requests across 35 contributors since v2.0.0.

## Key Features

- **Native GGUF import** — `coli import model.gguf` loads any GGUF without conversion on CPU, Vulkan, and CUDA
- **Multi-platform GPU** — Vulkan (Linux + Windows), CUDA for NVIDIA (compute 8.0+), Metal for Apple Silicon
- **Long-context support** — Qwen3.8-Flash-Next at 262,144 tokens; speculative decoding via Qwen3.6's MTP head on all backends
- **KV cache float16** — halved RAM versus prior releases; GLM-5.3 at 131K context cut from 23.9 GB to 11.9 GB
- **New chat UI** — `coli ui` adds reasoning blocks, image input, web search, a live expert map, and coding-agent support

## Quick Start

```bash
git clone https://github.com/JustVugg/colibri.git && cd colibri
./start-here.sh   # detects platform, downloads Qwen3.6-35B-A3B (23 GB) and builds
coli chat         # starts interactive session
```

Or import any HuggingFace GGUF:
```bash
hf download unsloth/DeepSeek-V4.1-Flash-1017-GGUF --include "UD-IQ1_S/*" --local-dir v41
coli import v41/UD-IQ1_S/DeepSeek-V4.1-Flash-1017-UD-IQ1_S-00001-of-00005.gguf
COLI_VULKAN=1 coli chat --model DeepSeek-V4.1-Flash-1017-UD-IQ1_S.colibri
```

## The Verdict

Colibri is for developers who want a frontier-class model on hardware they own and don't want to manage a Python virtualenv to do it. The native GGUF support makes v2.1.0 the first version that works with the mainstream Hugging Face model ecosystem rather than requiring you to convert or download from the project's own sources — that's the change that turns a niche project into a general-purpose tool. Skip it if you need OpenAI API compatibility, production throughput, or a model Colibri doesn't yet support; llama.cpp still has the broader model roster. But for anyone running a consumer GPU or a beefy CPU who wants to run a 100B+ model locally without touching Python, v2.1.0 is the reason to try it.

📎 [GitHub](https://github.com/JustVugg/colibri) · [v2.1.0 Release](https://github.com/JustVugg/colibri/releases/tag/v2.1.0) · [Homepage](https://justvugg.github.io/colibri/)