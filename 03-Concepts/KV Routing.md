---
type: "concept"
area: "[[Inference Infrastructure]]"
difficulty: 4
mastery: 0
prerequisites: ["[[KV Cache]]", "[[RadixAttention and Prefix Caching]]", "[[Model Routing]]"]
unlocks: ["[[Disaggregated Serving]]"]
tags: ["concept", "area/inference-infrastructure"]
---

# KV Routing

Routing a request to the replica that already holds (or is best placed to build) the relevant KV — so prefix reuse and disaggregated decode actually pay off. A distributed-systems problem: locality-aware load balancing over stateful workers.

> [!info] Why it matters for an infra engineer
> Once KV is the valuable state, routing to where it lives is the whole game. This is consistent-hashing/cache-locality thinking applied to GPUs.

## Related

- **Area:** [[Inference Infrastructure]]
- **Prerequisites:** [[KV Cache]], [[RadixAttention and Prefix Caching]], [[Model Routing]]
- **Unlocks:** [[Disaggregated Serving]]
- **Studied in:** [[Week 30 — Disaggregated serving — Dynamo & llm-d]], [[Week 42 — Distributed inference at scale]]
- **Resources:** [[NVIDIA Dynamo Documentation]], [[dynamo]]
- **Projects:** [[Level 6 — Distributed inference cluster]]

## Notes
