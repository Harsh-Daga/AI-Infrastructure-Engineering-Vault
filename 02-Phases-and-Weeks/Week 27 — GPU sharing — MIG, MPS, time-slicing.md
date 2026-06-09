---
type: "week"
week: 27
phase: "Phase 4 — GPU Orchestration & the AI Platform on Kubernetes"
status: "not-started"
start: 
end: 
objective: "GPU sharing: MIG (hard isolation), MPS (soft sharing), time-slicing."
concepts: ["[[GPU Sharing (MIG and MPS)]]"]
project: ["[[Level 4 — AI platform on Kubernetes]]", "[[Level 5 — GPU scheduling deep-dive]]"]
deliverable: 
tags: ["week", "phase/4"]
---

# Week 27 — GPU sharing — MIG, MPS, time-slicing

**Phase:** [[Phase 4 — GPU Orchestration & the AI Platform on Kubernetes]]  
**Objective:** GPU sharing: MIG (hard isolation), MPS (soft sharing), time-slicing.  
**Concepts:** [[GPU Sharing (MIG and MPS)]]
**Project:** [[Level 4 — AI platform on Kubernetes]], [[Level 5 — GPU scheduling deep-dive]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
NVIDIA MIG/MPS docs; a "MIG vs MPS vs time-slicing" comparison.

1. Read NVIDIA MIG/MPS docs.
2. Learn MIG (hard) vs MPS (soft) vs time-slicing (none) isolation.
3. Write which gives memory isolation and which doesn't.

## Read (15m)
A writeup quantifying utilization/cost gains from MIG on inference nodes.

1. Read a writeup quantifying MIG utilization gains.
2. Note the cost-per-request improvement on inference nodes.
3. Write when MIG backfires (fixed slice sizes).

## Build (20m)
Partition a GPU with MIG (or simulate with time-slicing); schedule two small models on one physical GPU; measure isolation.

## Step-by-step
1. On an A100/H100, enable MIG and create profiles (e.g. 7×1g or 3×2g) — or use time-slicing if no MIG.
2. Expose the slices to Kubernetes via the GPU Operator's MIG/time-slicing config.
3. Schedule two small models onto one physical GPU.
4. Stress one model and measure whether the other's latency is affected (isolation test).
5. Compute cost-per-request with sharing vs a dedicated GPU per model.

## Reflect (5m)
> For small-model inference, why can MIG cut cost-per-request dramatically — and when does it backfire?

## Done when
- [ ] Two models running on one physical GPU.
- [ ] An isolation measurement (MIG hard vs MPS/time-slicing soft).
- [ ] A cost-per-request comparison vs dedicated GPUs.

## Common pitfalls
- Time-slicing gives no memory isolation — one model can OOM the other.
- MIG profiles are fixed-size; a model that doesn't fit a slice wastes the remainder.

## Resources
- [[NVIDIA GPU Operator Documentation]]

## Go deeper
- NVIDIA MIG/MPS docs.
- A "MIG vs MPS vs time-slicing" comparison with utilization numbers.

## Tasks
- [ ] Study/open [[NVIDIA GPU Operator Documentation]]
- [ ] **Build:** Partition a GPU with MIG (or simulate with time-slicing); schedule two small models on one physical GPU; measure isolation.
- [ ] Two models running on one physical GPU.
- [ ] An isolation measurement (MIG hard vs MPS/time-slicing soft).
- [ ] A cost-per-request comparison vs dedicated GPUs.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
