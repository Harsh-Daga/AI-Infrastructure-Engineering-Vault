---
type: "concept"
area: "[[Distributed Training]]"
difficulty: 4
mastery: 0
prerequisites: ["[[Collective Communication (NCCL)]]", "[[NVLink and NVSwitch]]"]
unlocks: []
tags: ["concept", "area/distributed-training"]
---

# Tensor Parallelism

Split individual layers (matmuls) across GPUs, exchanging activations via collectives every layer — so it needs very fast interconnect and is normally kept **intra-node** over NVLink. Used both for training and for serving models too big for one GPU.

> [!info] Why it matters for an infra engineer
> TP is how you serve a model that won't fit on one GPU. Its scaling efficiency is set entirely by NVLink bandwidth.

## Related

- **Area:** [[Distributed Training]]
- **Prerequisites:** [[Collective Communication (NCCL)]], [[NVLink and NVSwitch]]
- **Studied in:** [[Week 16 — Multi-GPU single-node serving]], [[Week 37 — Parallelism taxonomy for training]]
- **Resources:** [[Megatron-LM]], [[Hugging Face Ultra-Scale Playbook]], [[Megatron-LM]]

## Notes
