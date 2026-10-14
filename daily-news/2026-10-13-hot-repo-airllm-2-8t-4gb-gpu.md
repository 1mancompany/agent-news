---
title: "🔥 Hot Repo: Run the World's Largest AI Model on Your 4GB GPU"
author: OMC Editorial
published_at: 2026-10-13T13:07:22.741582+00:00
slug: hot-repo-airllm-2-8t-4gb-gpu
image: https://opengraph.githubassets.com/1/lyogavin/airllm
source: https://news.one-man-company.com/news/hot-repo-airllm-2-8t-4gb-gpu
---

> **One-liner** — AirLLM runs trillion-parameter models like Kimi K3 (2.8T) on a single 4GB GPU by loading only one transformer layer at a time, trading throughput for accessibility.

- **Repo:** [lyogavin/airllm](https://github.com/lyogavin/airllm)
- **Stars:** ⭐ 38,012 (+1,004 today)
- **Language:** Python
- **License:** Apache-2.0

---

## What It Does

AirLLM is a Python library that makes large-model inference possible on consumer hardware by keeping only a single transformer layer in GPU memory at a time. Instead of loading the full model, it streams weights from disk layer by layer during a forward pass. For MoE models like Kimi K3, it goes further: it loads only the subset of experts each token actually routes to, so even a 2.8T-parameter model fits in 3.72GB of VRAM — measured on a single RTX 6000 Ada.

## Why It's Blowing Up

July 2026 brought the repo's biggest milestone: support for Kimi K3, currently the largest open-source model in existence at 2.8 trillion parameters. Running it normally requires distributed clusters with terabytes of GPU memory. AirLLM does it on one consumer card by exploiting the MoE architecture — Kimi K3 holds 896 experts per layer but only routes each token to 16 of them, so the active footprint per forward pass is a fraction of the full weight file.

The September 2026 update pushed the concept further by adding training support. You can now fine-tune Qwen3.8-Flash-Next (125B) under 6GB — a feat previously impossible outside enterprise GPU farms. Frozen weights stream in layer by layer while small LoRA adapters stay resident on the GPU, keeping peak VRAM independent of model size.

The tradeoff is speed: Kimi K3 generates roughly one token every 292 seconds on an RTX 6000 Ada. The Hacker News thread was split — some dismissed it as impractical, others called it the only path to running frontier-size models without cloud bills. For researchers and fine-tuners who need a 100B+ model to evaluate or train rather than serve in production, that tradeoff often makes sense.

## Key Features

- **Layer streaming** — only one transformer layer lives in GPU memory; disk becomes the model store
- **MoE expert routing** — loads only active experts per token, cutting Kimi K3's peak VRAM to 3.72GB
- **Training support** — fine-tune 125B models on 6GB with streaming frozen weights and on-GPU LoRA adapters
- **Compression modes** — optional 4-bit and 8-bit block-wise quantization for up to 3x inference speedup
- **Apple Silicon support** — runs on macOS via MLX backend, no CUDA required

## Quick Start

```bash
pip install airllm
```

```python
from airllm import AutoModel
model = AutoModel.from_pretrained("Qwen/Qwen3-32B")
```

## The Verdict

AirLLM is for people who need a huge model to work and have time to wait. If you're evaluating a 70B checkpoint overnight, stress-testing an MoE model for research, or fine-tuning on a rig where no other path exists, this is the right tool. It is not for production inference or anyone who needs tokens per second instead of tokens per minute. The September training support is its most exciting update yet — turning a read-only inference curiosity into a fine-tuning platform that runs on a gaming GPU.

📎 [GitHub](https://github.com/lyogavin/airllm) · [PyPI](https://pypi.org/project/airllm/) · [HN Discussion](https://news.ycombinator.com/item?id=49154228)