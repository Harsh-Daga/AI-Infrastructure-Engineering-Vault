---
type: "concept"
area: "[[Distributed Training]]"
difficulty: 4
mastery: 0
prerequisites: ["[[Attention]]", "[[Collective Communication (NCCL)]]"]
unlocks: []
tags: ["concept", "area/distributed-training"]
---

# Context Parallelism

Split a single long sequence across GPUs so attention over very long contexts fits and parallelizes. Increasingly important as context windows grow.

> [!info] Why it matters for an infra engineer
> Long-context workloads (and reasoning models) make this a real lever. It's part of the 5D-parallelism vocabulary you need.

## Related

- **Area:** [[Distributed Training]]
- **Prerequisites:** [[Attention]], [[Collective Communication (NCCL)]]
- **Studied in:** [[Week 37 — Parallelism taxonomy for training]]
- **Resources:** [[Hugging Face Ultra-Scale Playbook]]

## Notes
