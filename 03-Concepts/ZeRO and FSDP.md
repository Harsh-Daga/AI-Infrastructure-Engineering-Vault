---
type: "concept"
area: "[[Distributed Training]]"
difficulty: 4
mastery: 0
prerequisites: ["[[Data Parallelism]]", "[[GPU Memory Hierarchy]]"]
unlocks: []
tags: ["concept", "area/distributed-training"]
---

# ZeRO and FSDP

Shard optimizer state, gradients, and parameters across data-parallel ranks (ZeRO stages 1–3 / PyTorch FSDP2) so a model that won't fit on one GPU still trains, gathering shards just-in-time. DeepSpeed Infinity adds CPU/NVMe offload.

> [!info] Why it matters for an infra engineer
> FSDP2/TorchTitan is the PyTorch-native way large models actually get trained. You operate these even if you never write the training loop.

## Related

- **Area:** [[Distributed Training]]
- **Prerequisites:** [[Data Parallelism]], [[GPU Memory Hierarchy]]
- **Studied in:** [[Week 37 — Parallelism taxonomy for training]], [[Week 38 — Training frameworks — Megatron, FSDP2, DeepSpeed]]
- **Resources:** [[ZeRO (DeepSpeed)]], [[PyTorch FSDP]], [[DeepSpeed]], [[torchtitan]], [[Hugging Face Ultra-Scale Playbook]]

## Notes
