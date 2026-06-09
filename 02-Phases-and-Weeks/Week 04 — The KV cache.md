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

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
vLLM PagedAttention paper talk / blog; any solid "KV cache explained" engineering post.

## Read (15m)
vLLM blog: "Efficient Memory Management for LLM Serving with PagedAttention."

## Build (20m)
With vLLM or llama.cpp, vary batch size and context; observe KV memory and throughput. Find the OOM cliff.

## Step-by-step
1. With vLLM or llama.cpp, serve a 7–8B model and note baseline KV memory at idle.
2. Sweep batch size and context length; after each, record KV memory and throughput.
3. Push until you hit the out-of-memory cliff; note the (batch × context) product where it breaks.
4. Compute theoretical KV bytes and compare to observed — reconcile the gap (paging, fragmentation).
5. Sketch a tiered KV store (GPU→CPU→SSD): what you'd cache, evict, and how you'd index it.

## Reflect (5m)
> If you had to design a tiered store for KV (GPU→CPU→SSD), what would you cache and evict?

## Done when
- [ ] You found and recorded the OOM cliff for your setup.
- [ ] Your computed KV size is within a small factor of observed memory.
- [ ] You have a one-paragraph tiered-KV design with an eviction policy.

## Common pitfalls
- `gpu-memory-utilization` set too high leaves no headroom for activations → spurious OOM.
- PagedAttention block size affects fragmentation; the naive formula slightly under-counts.

## Resources
- [[vLLM Blog — PagedAttention]]
- [[PagedAttention (vLLM)]]
- [[vllm]]
- [[llama.cpp]]

## Go deeper
- vLLM paper: "Efficient Memory Management for LLM Serving with PagedAttention."
- LMCache / KV-offload writeups — what a real tiered KV store looks like.

## Tasks
- [ ] Study/open [[vLLM Blog — PagedAttention]]
- [ ] Study/open [[PagedAttention (vLLM)]]
- [ ] Study/open [[vllm]]
- [ ] Study/open [[llama.cpp]]
- [ ] **Build:** With vLLM or llama.cpp, vary batch size and context; observe KV memory and throughput. Find the OOM cliff.
- [ ] You found and recorded the OOM cliff for your setup.
- [ ] Your computed KV size is within a small factor of observed memory.
- [ ] You have a one-paragraph tiered-KV design with an eviction policy.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
