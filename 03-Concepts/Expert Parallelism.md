---
type: "concept"
area: "[[Distributed Training]]"
difficulty: 4
mastery: 0
prerequisites: ["[[Mixture of Experts]]", "[[Collective Communication (NCCL)]]"]
unlocks: []
tags: ["concept", "area/distributed-training"]
---

# Expert Parallelism

Shard MoE experts across GPUs; tokens are dispatched to their experts via **all-to-all** comms and combined back. The all-to-all is the network-heavy signature of MoE serving/training.

> [!info] Why it matters for an infra engineer
> Expert parallelism is where MoE meets the fabric. It's why MoE models stress all-to-all bandwidth specifically.

## Related

- **Area:** [[Distributed Training]]
- **Prerequisites:** [[Mixture of Experts]], [[Collective Communication (NCCL)]]
- **Studied in:** [[Week 08 — Model families & what they cost to run]], [[Week 37 — Parallelism taxonomy for training]]
- **Resources:** [[Switch Transformer & GShard (MoE)]], [[Hugging Face Ultra-Scale Playbook]]

## Notes
