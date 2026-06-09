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

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
Megatron-Core docs; PyTorch FSDP2 / TorchTitan docs.

## Read (15m)
A "how we trained a 70B model" engineering report focused on the systems side.

## Build (20m)
Launch a multi-node-style training run (even 2 small nodes rented hourly) with one framework; capture a profile/timeline.

## Step-by-step
1. Pick one framework (Megatron-Core, FSDP2/TorchTitan, or DeepSpeed) and a small model.
2. Launch a multi-node-style run (even 2 small nodes rented hourly).
3. Capture a profile/timeline of one training step.
4. Break the step into compute / comms / data-loading and find the dominant cost.

## Reflect (5m)
> Where does the time actually go in a training step — compute, comms, or data loading?

## Done when
- [ ] A multi-node training run completed with a captured step profile.
- [ ] A breakdown of where step time goes (compute vs comms vs data).
- [ ] You can compare the framework's ergonomics vs the others conceptually.

## Common pitfalls
- Data loading often stalls the GPUs; check it before blaming the model or comms.
- Launcher/rendezvous misconfig (ranks, master addr) is the usual reason runs hang at start.

## Resources
- [[Megatron-LM]]
- [[torchtitan]]
- [[DeepSpeed]]
- [[PyTorch FSDP]]
- [[Meta Engineering & PyTorch Blog]]

## Go deeper
- Megatron-Core docs; PyTorch FSDP2 / TorchTitan docs.
- A "how we trained a 70B model" systems-focused report.

## Tasks
- [ ] Study/open [[Megatron-LM]]
- [ ] Study/open [[torchtitan]]
- [ ] Study/open [[DeepSpeed]]
- [ ] Study/open [[PyTorch FSDP]]
- [ ] Study/open [[Meta Engineering & PyTorch Blog]]
- [ ] **Build:** Launch a multi-node-style training run (even 2 small nodes rented hourly) with one framework; capture a profile/timeline.
- [ ] A multi-node training run completed with a captured step profile.
- [ ] A breakdown of where step time goes (compute vs comms vs data).
- [ ] You can compare the framework's ergonomics vs the others conceptually.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
