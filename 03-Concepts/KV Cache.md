---
type: "concept"
area: "[[Inference Infrastructure]]"
difficulty: 3
mastery: 0
prerequisites: ["[[Attention]]", "[[Transformer Block]]", "[[GPU Memory Hierarchy]]"]
unlocks: ["[[Agent Memory]]", "[[Continuous Batching]]", "[[Disaggregated Serving]]", "[[KV Offload]]", "[[KV Routing]]", "[[PagedAttention]]", "[[Prefill vs Decode]]", "[[RadixAttention and Prefix Caching]]"]
tags: ["concept", "area/inference-infrastructure"]
---

# KV Cache

★ The single most important concept for an inference engineer. To avoid recomputing attention over the whole prefix every decode step, the model caches each token's key/value tensors. The KV cache grows with **batch × sequence length × layers × heads** and quickly dominates inference memory — it, not the weights, is what OOMs you under load. Every serving optimization (paging, prefix reuse, offload, disaggregation, KV routing) is a way to manage this one data structure.

> [!info] Why it matters for an infra engineer
> Understand the KV cache deeply and half the field clicks: PagedAttention, prefix caching, disaggregation, KV offload and routing are all KV-cache management.

## Related

- **Area:** [[Inference Infrastructure]]
- **Prerequisites:** [[Attention]], [[Transformer Block]], [[GPU Memory Hierarchy]]
- **Unlocks:** [[Agent Memory]], [[Continuous Batching]], [[Disaggregated Serving]], [[KV Offload]], [[KV Routing]], [[PagedAttention]], [[Prefill vs Decode]], [[RadixAttention and Prefix Caching]]
- **Studied in:** [[Week 04 — The KV cache]], [[Week 15 — KV cache management & offloading]]
- **Resources:** [[vLLM Blog — PagedAttention]], [[PagedAttention (vLLM)]]
- **Projects:** [[Level 1 — Run local LLMs]]

## Notes
