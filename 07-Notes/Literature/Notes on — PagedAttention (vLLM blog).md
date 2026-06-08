---
type: "literature"
source: "vLLM blog"
url: "https://blog.vllm.ai/2023/06/20/vllm.html"
author: "vLLM Project"
date-read: "2026-06-09"
tags: ["literature"]
---

# Notes on — PagedAttention (vLLM blog)

**Source:** [[vLLM Blog — PagedAttention]] · relates to the paper [[PagedAttention (vLLM)]]

## Summary
The KV cache is stored in fixed-size blocks like OS virtual-memory pages, eliminating fragmentation and enabling near-100% KV memory utilization and prefix sharing.

## Key takeaways
- Fragmentation, not raw size, was wasting most KV memory.
- Block tables + copy-on-write make prefix sharing cheap.

## How this connects
- [[KV Cache]] → [[PagedAttention]] → [[RadixAttention and Prefix Caching]]
- Applied in [[Week 04 — The KV cache]] and [[Level 1 — Run local LLMs]].
