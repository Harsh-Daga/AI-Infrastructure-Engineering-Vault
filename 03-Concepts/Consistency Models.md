---
type: "concept"
area: "[[Inference Infrastructure]]"
difficulty: 3
mastery: 0
prerequisites: ["[[CAP]]"]
unlocks: ["[[Checkpointing and Fault Tolerance]]", "[[Raft]]"]
tags: ["concept", "area/inference-infrastructure"]
---

# Consistency Models

Strong vs eventual vs causal consistency, linearizability, and the coordination cost of each. Directly applicable to distributed KV/checkpoint stores and to worker registration/discovery in disaggregated serving.

> [!info] Why it matters for an infra engineer
> Choosing a consistency model is choosing your failure modes. It's the difference between a discovery service that's correct and one that's subtly wrong.

## Related

- **Area:** [[Inference Infrastructure]]
- **Prerequisites:** [[CAP]]
- **Unlocks:** [[Checkpointing and Fault Tolerance]], [[Raft]]
- **Studied in:** [[Week 36 — Distributed systems for AI — coordination]]
- **Resources:** [[Designing Data-Intensive Applications]], [[MIT 6.824 Distributed Systems]]

## Notes
