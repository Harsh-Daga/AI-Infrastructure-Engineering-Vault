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

## Learn (20m)
NVIDIA MIG/MPS docs; a "MIG vs MPS vs time-slicing" comparison.

## Read (15m)
A writeup quantifying utilization/cost gains from MIG on inference nodes.

## Build (20m)
Partition a GPU with MIG (or simulate with time-slicing); schedule two small models on one physical GPU; measure isolation.

## Reflect (5m)
> For small-model inference, why can MIG cut cost-per-request dramatically — and when does it backfire?

## Resources
- [[NVIDIA GPU Operator Documentation]]

## Tasks
- [ ] Study/open [[NVIDIA GPU Operator Documentation]]
- [ ] **Build:** Partition a GPU with MIG (or simulate with time-slicing); schedule two small models on one physical GPU; measure isolation.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
