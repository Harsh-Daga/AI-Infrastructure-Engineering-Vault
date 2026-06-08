---
type: "project"
level: 1
status: "not-started"
phase: "[[Phase 1 — Foundations]]"
skills: ["[[KV Cache]]", "[[Quantization]]", "[[Prefill vs Decode]]", "[[GPU Memory Hierarchy]]", "[[TTFT vs ITL]]", "[[Continuous Batching]]"]
repos: ["[[ollama]]", "[[llama.cpp]]", "[[vllm]]"]
success-criteria: "You can predict, before running, whether a given model+context+batch will fit, and you can explain why decode is bandwidth-bound."
tags: ["project", "level/1"]
---

# Level 1 — Run local LLMs

**Phase:** [[Phase 1 — Foundations]]  
**Weeks:** [[Week 01 — How an LLM actually runs]], [[Week 02 — Tokenization, embeddings, context windows]], [[Week 03 — Attention & the transformer, infra lens]], [[Week 04 — The KV cache]], [[Week 05 — GPU architecture & memory hierarchy]], [[Week 06 — Precision & quantization]], [[Week 07 — Where the GPU time goes — profiling]], [[Week 08 — Model families & what they cost to run]]

## Architecture
Single machine/GPU. Ollama + llama.cpp + a basic vLLM server.

## Components
model runtime, a tiny benchmark harness, `nvidia-smi` logging.

## Why it matters
Builds the GPU/serving intuition everything else rests on; you feel the OOM cliff and the bandwidth wall yourself.

## Skills learned
GPU memory behavior, quantization tradeoffs, TTFT vs throughput, the KV cache in practice.

## Skills (concept links)

- [[KV Cache]]
- [[Quantization]]
- [[Prefill vs Decode]]
- [[GPU Memory Hierarchy]]
- [[TTFT vs ITL]]
- [[Continuous Batching]]

## Success criteria
> You can predict, before running, whether a given model+context+batch will fit, and you can explain why decode is bandwidth-bound.

## Repos to study
[[ollama]], [[llama.cpp]], [[vllm]]

## Build log
_Log progress here as you build._


## Tasks
- [ ] Scaffold the repo with a real README and architecture doc
- [ ] Implement the core architecture above
- [ ] Produce the benchmark / cost model that proves the success criteria
- [ ] Write the "what I learned" section and publish to the learning log
