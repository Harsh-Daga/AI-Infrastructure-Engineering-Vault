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

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
Hugging Face "Ultra-Scale Playbook" (the single best free resource on this); the Megatron-LM parallelism docs.

## Read (15m)
The Megatron-LM and ZeRO papers (architecture + results sections).

## Build (20m)
Run a small multi-GPU training job with FSDP2 (or DeepSpeed ZeRO); shard a model that wouldn't fit on one GPU.

## Step-by-step
1. Read the Ultra-Scale Playbook sections on each parallelism axis.
2. On a multi-GPU node, run a small FSDP2 (or DeepSpeed ZeRO) training job.
3. Shard a model that wouldn't fit on one GPU; confirm it now fits and trains a step.
4. For your model+cluster, write down the parallelism mix you'd choose and the tradeoff per axis.

## Reflect (5m)
> For a given model + cluster, how do you choose the parallelism mix? What's the tradeoff each axis makes?

## Done when
- [ ] A model that doesn't fit on one GPU successfully sharded and training.
- [ ] A written parallelism-mix choice with the tradeoff each axis makes.
- [ ] You can place a job in the data/tensor/pipeline/expert taxonomy.

## Common pitfalls
- Tensor parallelism is comms-heavy — keep it intra-node; data parallelism scales out best.
- ZeRO stages trade memory for communication; stage-3 saves the most memory but talks the most.

## Resources
- [[Hugging Face Ultra-Scale Playbook]]
- [[Megatron-LM]]
- [[ZeRO (DeepSpeed)]]
- [[Megatron-LM]]

## Go deeper
- Hugging Face Ultra-Scale Playbook (the single best free resource).
- The Megatron-LM and ZeRO papers (architecture + results).

## Tasks
- [ ] Study/open [[Hugging Face Ultra-Scale Playbook]]
- [ ] Study/open [[Megatron-LM]]
- [ ] Study/open [[ZeRO (DeepSpeed)]]
- [ ] Study/open [[Megatron-LM]]
- [ ] **Build:** Run a small multi-GPU training job with FSDP2 (or DeepSpeed ZeRO); shard a model that wouldn't fit on one GPU.
- [ ] A model that doesn't fit on one GPU successfully sharded and training.
- [ ] A written parallelism-mix choice with the tradeoff each axis makes.
- [ ] You can place a job in the data/tensor/pipeline/expert taxonomy.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
