---
type: "concept"
area: "[[Inference Infrastructure]]"
difficulty: 4
mastery: 0
prerequisites: ["[[KV Cache]]", "[[GPU Memory Hierarchy]]"]
unlocks: []
tags: ["concept", "area/inference-infrastructure"]
---

# KV Offload

Tiering the KV cache beyond GPU HBM: GPU → CPU RAM → local SSD → network storage, with eviction policy. Lets you serve longer contexts / more concurrency than HBM alone allows, at the cost of transfer latency (the classic cache-tiering tradeoff).

> [!info] Why it matters for an infra engineer
> It's a memory-hierarchy and eviction problem you already understand from CPU caches — now applied to the hottest data structure in inference.

## Related

- **Area:** [[Inference Infrastructure]]
- **Prerequisites:** [[KV Cache]], [[GPU Memory Hierarchy]]
- **Studied in:** [[Week 15 — KV cache management & offloading]]
- **Resources:** [[vLLM Documentation]]

## Notes
