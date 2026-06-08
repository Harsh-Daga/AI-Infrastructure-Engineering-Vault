---
type: "concept"
area: "[[Inference Infrastructure]]"
difficulty: 5
mastery: 0
prerequisites: ["[[Prefill vs Decode]]", "[[KV Cache]]", "[[KV Routing]]", "[[RDMA]]", "[[Collective Communication (NCCL)]]"]
unlocks: []
tags: ["concept", "area/inference-infrastructure"]
---

# Disaggregated Serving

The defining 2026 architecture: run prefill and decode on **separate GPU pools**, connected by RDMA KV-cache transport (NIXL), scaled and tuned independently (the xPyD ratio). Orchestrated by NVIDIA Dynamo or the K8s-native llm-d. Inference becomes "a graph of coordinated services" — routing, KV placement, discovery, autoscaling, fault handling.

> [!info] Why it matters for an infra engineer
> This is a distributed-systems job — exactly your background. Building it hands-on is rare and immediately credible.

## Related

- **Area:** [[Inference Infrastructure]]
- **Prerequisites:** [[Prefill vs Decode]], [[KV Cache]], [[KV Routing]], [[RDMA]], [[Collective Communication (NCCL)]]
- **Studied in:** [[Week 30 — Disaggregated serving — Dynamo & llm-d]], [[Week 42 — Distributed inference at scale]]
- **Resources:** [[NVIDIA Dynamo Documentation]], [[DistServe & Splitwise]], [[dynamo]], [[llm-d]]
- **Projects:** [[Level 6 — Distributed inference cluster]]

## Notes
