---
type: "week"
week: 38
phase: "Phase 5 — Networking, Distributed Systems for AI, Distributed Training"
status: "not-started"
start: 
end: 
objective: "Training frameworks: Megatron-Core, FSDP2/TorchTitan, DeepSpeed."
concepts: ["[[ZeRO and FSDP]]", "[[Tensor Parallelism]]", "[[Pipeline Parallelism]]"]
project: []
deliverable: 
tags: ["week", "phase/5"]
---

# Week 38 — Training frameworks — Megatron, FSDP2, DeepSpeed

**Phase:** [[Phase 5 — Networking, Distributed Systems for AI, Distributed Training]]  
**Objective:** Training frameworks: Megatron-Core, FSDP2/TorchTitan, DeepSpeed.  
**Concepts:** [[ZeRO and FSDP]], [[Tensor Parallelism]], [[Pipeline Parallelism]]

## Learn (20m)
Megatron-Core docs; PyTorch FSDP2 / TorchTitan docs.

## Read (15m)
A "how we trained a 70B model" engineering report focused on the systems side.

## Build (20m)
Launch a multi-node-style training run (even 2 small nodes rented hourly) with one framework; capture a profile/timeline.

## Reflect (5m)
> Where does the time actually go in a training step — compute, comms, or data loading?

## Resources
- [[Megatron-LM]]
- [[torchtitan]]
- [[DeepSpeed]]
- [[PyTorch FSDP]]
- [[Meta Engineering & PyTorch Blog]]

## Tasks
- [ ] Study/open [[Megatron-LM]]
- [ ] Study/open [[torchtitan]]
- [ ] Study/open [[DeepSpeed]]
- [ ] Study/open [[PyTorch FSDP]]
- [ ] Study/open [[Meta Engineering & PyTorch Blog]]
- [ ] **Build:** Launch a multi-node-style training run (even 2 small nodes rented hourly) with one framework; capture a profile/timeline.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
