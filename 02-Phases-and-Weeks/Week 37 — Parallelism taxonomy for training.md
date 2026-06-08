---
type: "week"
week: 37
phase: "Phase 5 — Networking, Distributed Systems for AI, Distributed Training"
status: "not-started"
start: 
end: 
objective: "★ Parallelism taxonomy for training: data/tensor/pipeline/context/expert; 3D/5D; ZeRO/FSDP."
concepts: ["[[Data Parallelism]]", "[[Tensor Parallelism]]", "[[Pipeline Parallelism]]", "[[Context Parallelism]]", "[[Expert Parallelism]]", "[[ZeRO and FSDP]]"]
project: []
deliverable: 
tags: ["week", "phase/5"]
---

# Week 37 — Parallelism taxonomy for training

**Phase:** [[Phase 5 — Networking, Distributed Systems for AI, Distributed Training]]  
**Objective:** ★ Parallelism taxonomy for training: data/tensor/pipeline/context/expert; 3D/5D; ZeRO/FSDP.  
**Concepts:** [[Data Parallelism]], [[Tensor Parallelism]], [[Pipeline Parallelism]], [[Context Parallelism]], [[Expert Parallelism]], [[ZeRO and FSDP]]

## Learn (20m)
Hugging Face "Ultra-Scale Playbook" (the single best free resource on this); the Megatron-LM parallelism docs.

## Read (15m)
The Megatron-LM and ZeRO papers (architecture + results sections).

## Build (20m)
Run a small multi-GPU training job with FSDP2 (or DeepSpeed ZeRO); shard a model that wouldn't fit on one GPU.

## Reflect (5m)
> For a given model + cluster, how do you choose the parallelism mix? What's the tradeoff each axis makes?

## Resources
- [[Hugging Face Ultra-Scale Playbook]]
- [[Megatron-LM]]
- [[ZeRO (DeepSpeed)]]
- [[Megatron-LM]]

## Tasks
- [ ] Study/open [[Hugging Face Ultra-Scale Playbook]]
- [ ] Study/open [[Megatron-LM]]
- [ ] Study/open [[ZeRO (DeepSpeed)]]
- [ ] Study/open [[Megatron-LM]]
- [ ] **Build:** Run a small multi-GPU training job with FSDP2 (or DeepSpeed ZeRO); shard a model that wouldn't fit on one GPU.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
