---
type: "week"
week: 11
phase: "Phase 2 — LLM Serving, Deep"
status: "not-started"
start: 
end: 
objective: "SGLang & RadixAttention: automatic prefix caching, when shared-prefix workloads win big."
concepts: ["[[RadixAttention and Prefix Caching]]"]
project: []
deliverable: 
tags: ["week", "phase/2"]
---

# Week 11 — SGLang & RadixAttention

**Phase:** [[Phase 2 — LLM Serving, Deep]]  
**Objective:** SGLang & RadixAttention: automatic prefix caching, when shared-prefix workloads win big.  
**Concepts:** [[RadixAttention and Prefix Caching]]

## Learn (20m)
SGLang docs + the RadixAttention blog.

## Read (15m)
SGLang vs vLLM benchmark posts (note the workload-dependence of the result).

## Build (20m)
Construct a shared-prefix workload (same long system prompt, many queries); compare SGLang vs vLLM TTFT.

## Reflect (5m)
> What property of your workload decides whether prefix caching matters?

## Resources
- [[SGLang Documentation]]
- [[RadixAttention (SGLang)]]
- [[sglang]]
- [[SGLang Blog]]

## Tasks
- [ ] Study/open [[SGLang Documentation]]
- [ ] Study/open [[RadixAttention (SGLang)]]
- [ ] Study/open [[sglang]]
- [ ] Study/open [[SGLang Blog]]
- [ ] **Build:** Construct a shared-prefix workload (same long system prompt, many queries); compare SGLang vs vLLM TTFT.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
