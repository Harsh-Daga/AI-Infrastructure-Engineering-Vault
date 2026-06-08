---
type: "concept"
area: "[[AI Reliability Engineering]]"
difficulty: 4
mastery: 0
prerequisites: ["[[Data Parallelism]]", "[[Consistency Models]]"]
unlocks: ["[[AI Reliability Engineering]]", "[[Stragglers and SDC]]"]
tags: ["concept", "area/ai-reliability-engineering"]
---

# Checkpointing and Fault Tolerance

Distributed/async checkpointing and restart for stateful, synchronous training. At scale a node *will* die mid-run; checkpoint interval is an economic decision (work lost vs I/O cost). Elastic training (TorchElastic) lets a run continue with fewer ranks.

> [!info] Why it matters for an infra engineer
> At 1,000 GPUs the gap between a 5-minute and 30-minute checkpoint interval is real money per node failure. This is your SRE instinct applied to training.

## Related

- **Area:** [[AI Reliability Engineering]]
- **Prerequisites:** [[Data Parallelism]], [[Consistency Models]]
- **Unlocks:** [[AI Reliability Engineering]], [[Stragglers and SDC]]
- **Studied in:** [[Week 39 — Checkpointing, fault tolerance, elastic training]]
- **Resources:** [[Meta Engineering & PyTorch Blog]], [[Designing Data-Intensive Applications]]
- **Projects:** [[Level 7 — Production-grade AI platform]]

## Notes
