---
type: "week"
week: 15
phase: "Phase 2 — LLM Serving, Deep"
status: "not-started"
start: 
end: 
objective: "KV cache management & offloading: prefix caching, KV reuse, offload to CPU/SSD, eviction."
concepts: ["[[KV Offload]]", "[[RadixAttention and Prefix Caching]]", "[[KV Cache]]"]
project: []
deliverable: 
tags: ["week", "phase/2"]
---

# Week 15 — KV cache management & offloading

**Phase:** [[Phase 2 — LLM Serving, Deep]]  
**Objective:** KV cache management & offloading: prefix caching, KV reuse, offload to CPU/SSD, eviction.  
**Concepts:** [[KV Offload]], [[RadixAttention and Prefix Caching]], [[KV Cache]]

## Learn (20m)
vLLM automatic prefix caching docs; KV-offload writeups (e.g. LMCache-style).

## Read (15m)
A blog on KV cache offload / tiered KV.

## Build (20m)
Enable prefix caching; build a workload that benefits (repeated system prompt) and measure cache hit rate vs latency.

## Reflect (5m)
> Design a global, cross-replica KV cache. What are the consistency and routing problems?

## Resources
- [[vLLM Documentation]]
- [[vLLM Blog]]

## Tasks
- [ ] Study/open [[vLLM Documentation]]
- [ ] Study/open [[vLLM Blog]]
- [ ] **Build:** Enable prefix caching; build a workload that benefits (repeated system prompt) and measure cache hit rate vs latency.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
