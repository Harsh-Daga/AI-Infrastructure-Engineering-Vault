---
type: "concept"
area: "[[AI Networking]]"
difficulty: 5
mastery: 0
prerequisites: ["[[GPU Memory Hierarchy]]"]
unlocks: ["[[Cluster Topology]]", "[[Context Parallelism]]", "[[Data Parallelism]]", "[[Disaggregated Serving]]", "[[Expert Parallelism]]", "[[Pipeline Parallelism]]", "[[Stragglers and SDC]]", "[[Tensor Parallelism]]"]
tags: ["concept", "area/ai-networking"]
---

# Collective Communication (NCCL)

★ The bridge concept. All-reduce, all-gather, reduce-scatter, broadcast, all-to-all are how GPUs exchange data. They bound **both** distributed training (gradient sync) and multi-GPU inference (tensor parallelism, KV transfer). Ring/tree algorithms; bandwidth and topology dominate. all-reduce is the operation that dominates data-parallel training time at scale.

> [!info] Why it matters for an infra engineer
> Collectives tie training and inference together. Master them and you understand why the network — not the GPU — often sets the scaling ceiling.

## Related

- **Area:** [[AI Networking]]
- **Prerequisites:** [[GPU Memory Hierarchy]]
- **Unlocks:** [[Cluster Topology]], [[Context Parallelism]], [[Data Parallelism]], [[Disaggregated Serving]], [[Expert Parallelism]], [[Pipeline Parallelism]], [[Stragglers and SDC]], [[Tensor Parallelism]]
- **Studied in:** [[Week 16 — Multi-GPU single-node serving]], [[Week 33 — Collective communication & NCCL]]
- **Resources:** [[nccl]], [[nccl-tests]], [[NVIDIA Deep Learning Institute (DLI)]], [[Hugging Face Ultra-Scale Playbook]]

## Notes
