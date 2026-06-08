---
type: "week"
week: 6
phase: "Phase 1 — Foundations"
status: "not-started"
start: 
end: 
objective: "Precision & quantization — your #1 inference lever: FP32/FP16/BF16/FP8/INT8/INT4 tradeoffs."
concepts: ["[[Quantization]]"]
project: ["[[Level 1 — Run local LLMs]]"]
deliverable: 
tags: ["week", "phase/1"]
---

# Week 06 — Precision & quantization

**Phase:** [[Phase 1 — Foundations]]  
**Objective:** Precision & quantization — your #1 inference lever: FP32/FP16/BF16/FP8/INT8/INT4 tradeoffs.  
**Concepts:** [[Quantization]]
**Project:** [[Level 1 — Run local LLMs]]

## Learn (20m)
Hugging Face quantization docs/blogs; a GPTQ/AWQ explainer.

## Read (15m)
An engineering writeup on FP8 inference results (e.g. serving-engine benchmark posts).

## Build (20m)
Serve the same model in FP16 vs FP8/INT4; compare VRAM, throughput, and output quality on a fixed prompt set.

## Reflect (5m)
> When is quantization free lunch, and when does it quietly cost you quality?

## Resources
- [[Hugging Face Blog]]
- [[vLLM Blog]]

## Tasks
- [ ] Study/open [[Hugging Face Blog]]
- [ ] Study/open [[vLLM Blog]]
- [ ] **Build:** Serve the same model in FP16 vs FP8/INT4; compare VRAM, throughput, and output quality on a fixed prompt set.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
