---
type: "week"
week: 4
phase: "Phase 1 — Foundations"
status: "not-started"
start: 
end: 
objective: "★ The KV cache: what it is, why it exists, how it grows, why it dominates inference memory."
concepts: ["[[KV Cache]]", "[[PagedAttention]]"]
project: ["[[Level 1 — Run local LLMs]]"]
deliverable: 
tags: ["week", "phase/1"]
---

# Week 04 — The KV cache

**Phase:** [[Phase 1 — Foundations]]  
**Objective:** ★ The KV cache: what it is, why it exists, how it grows, why it dominates inference memory.  
**Concepts:** [[KV Cache]], [[PagedAttention]]
**Project:** [[Level 1 — Run local LLMs]]

## Learn (20m)
vLLM PagedAttention paper talk / blog; any solid "KV cache explained" engineering post.

## Read (15m)
vLLM blog: "Efficient Memory Management for LLM Serving with PagedAttention."

## Build (20m)
With vLLM or llama.cpp, vary batch size and context; observe KV memory and throughput. Find the OOM cliff.

## Reflect (5m)
> If you had to design a tiered store for KV (GPU→CPU→SSD), what would you cache and evict?

## Resources
- [[vLLM Blog — PagedAttention]]
- [[PagedAttention (vLLM)]]
- [[vllm]]
- [[llama.cpp]]

## Tasks
- [ ] Study/open [[vLLM Blog — PagedAttention]]
- [ ] Study/open [[PagedAttention (vLLM)]]
- [ ] Study/open [[vllm]]
- [ ] Study/open [[llama.cpp]]
- [ ] **Build:** With vLLM or llama.cpp, vary batch size and context; observe KV memory and throughput. Find the OOM cliff.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
