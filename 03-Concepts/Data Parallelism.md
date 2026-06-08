---
type: "concept"
area: "[[Distributed Training]]"
difficulty: 3
mastery: 0
prerequisites: ["[[Collective Communication (NCCL)]]"]
unlocks: ["[[Checkpointing and Fault Tolerance]]", "[[ZeRO and FSDP]]"]
tags: ["concept", "area/distributed-training"]
---

# Data Parallelism

Replicate the model across GPUs, split the batch, and all-reduce gradients each step. The simplest scaling axis; its cost is the all-reduce, which grows with model size and GPU count.

> [!info] Why it matters for an infra engineer
> It's the baseline every other parallelism strategy is measured against, and the reason all-reduce bandwidth matters so much.

## Related

- **Area:** [[Distributed Training]]
- **Prerequisites:** [[Collective Communication (NCCL)]]
- **Unlocks:** [[Checkpointing and Fault Tolerance]], [[ZeRO and FSDP]]
- **Studied in:** [[Week 37 — Parallelism taxonomy for training]]
- **Resources:** [[Hugging Face Ultra-Scale Playbook]], [[ZeRO (DeepSpeed)]]

## Notes
