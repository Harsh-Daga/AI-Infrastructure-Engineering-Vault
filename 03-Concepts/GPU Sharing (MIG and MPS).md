---
type: "concept"
area: "[[GPU Orchestration]]"
difficulty: 4
mastery: 0
prerequisites: ["[[GPU Memory Hierarchy]]"]
unlocks: ["[[AI Cost Engineering]]"]
tags: ["concept", "area/gpu-orchestration"]
---

# GPU Sharing (MIG and MPS)

Three ways to put multiple workloads on one GPU: **MIG** (hardware-partitioned, hard isolation, multiple tenants), **MPS** (soft concurrent sharing), and time-slicing (the dev default). For small-model inference MIG can slash cost-per-request — until contention or fragmentation backfires.

> [!info] Why it matters for an infra engineer
> Fine-grained sharing is the lever that turns idle expensive GPUs into utilization. Knowing when MIG helps vs hurts is real cost engineering.

## Related

- **Area:** [[GPU Orchestration]]
- **Prerequisites:** [[GPU Memory Hierarchy]]
- **Unlocks:** [[AI Cost Engineering]]
- **Studied in:** [[Week 27 — GPU sharing — MIG, MPS, time-slicing]]
- **Resources:** [[NVIDIA GPU Operator Documentation]]
- **Projects:** [[Level 4 — AI platform on Kubernetes]], [[Level 5 — GPU scheduling deep-dive]]

## Notes
