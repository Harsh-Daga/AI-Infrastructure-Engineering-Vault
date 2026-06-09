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

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
vLLM automatic prefix caching docs; KV-offload writeups (e.g. LMCache-style).

1. Read vLLM automatic prefix caching docs.
2. Read an LMCache-style KV-offload writeup.
3. Write what gets cached, reused, and evicted in a tiered KV store.

## Read (15m)
A blog on KV cache offload / tiered KV.

1. Read a tiered-KV / KV-offload blog.
2. Note the latency cost of CPU/SSD offload vs the capacity gained.
3. Write when offload helps vs hurts.

## Build (20m)
Enable prefix caching; build a workload that benefits (repeated system prompt) and measure cache hit rate vs latency.

## Step-by-step
1. Enable vLLM automatic prefix caching (`--enable-prefix-caching`).
2. Build a workload with a repeated system prompt across many requests.
3. Measure cache hit rate, TTFT, and throughput vs the no-caching baseline.
4. If available, enable KV offload to CPU/SSD (LMCache-style) and re-measure under memory pressure.
5. Sketch a cross-replica global KV cache: routing, consistency, and eviction concerns.

## Reflect (5m)
> Design a global, cross-replica KV cache. What are the consistency and routing problems?

## Done when
- [ ] You measured cache hit rate vs latency improvement.
- [ ] You observed behavior under memory pressure with offload on.
- [ ] You have a one-paragraph global-KV design naming its hard problems.

## Common pitfalls
- Prefix cache only helps if requests truly share a prefix — measure the hit rate, don't assume it.
- Offload to SSD trades latency for capacity; the transfer can dominate for short contexts.

## Resources
- [[vLLM Documentation]]
- [[vLLM Blog]]

## Go deeper
- vLLM automatic prefix caching docs.
- An LMCache / tiered-KV blog post.

## Tasks
- [ ] Study/open [[vLLM Documentation]]
- [ ] Study/open [[vLLM Blog]]
- [ ] **Build:** Enable prefix caching; build a workload that benefits (repeated system prompt) and measure cache hit rate vs latency.
- [ ] You measured cache hit rate vs latency improvement.
- [ ] You observed behavior under memory pressure with offload on.
- [ ] You have a one-paragraph global-KV design naming its hard problems.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
