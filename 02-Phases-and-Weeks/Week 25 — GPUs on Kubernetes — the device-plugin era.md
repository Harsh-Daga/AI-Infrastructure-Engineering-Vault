---
type: "week"
week: 25
phase: "Phase 4 — GPU Orchestration & the AI Platform on Kubernetes"
status: "not-started"
start: 
end: 
objective: "GPUs on Kubernetes — the device-plugin era and why it's ending."
concepts: ["[[DRA]]", "[[GPU Sharing (MIG and MPS)]]"]
project: ["[[Level 4 — AI platform on Kubernetes]]"]
deliverable: 
tags: ["week", "phase/4"]
---

# Week 25 — GPUs on Kubernetes — the device-plugin era

**Phase:** [[Phase 4 — GPU Orchestration & the AI Platform on Kubernetes]]  
**Objective:** GPUs on Kubernetes — the device-plugin era and why it's ending.  
**Concepts:** [[DRA]], [[GPU Sharing (MIG and MPS)]]
**Project:** [[Level 4 — AI platform on Kubernetes]]

## Learn (20m)
NVIDIA GPU Operator docs; a "GPU scheduling on K8s, the old way" overview.

## Read (15m)
A 2026 piece on why the device-plugin model is being replaced.

## Build (20m)
On a GPU node (rent one hourly), install the NVIDIA GPU Operator; schedule a GPU pod; confirm with `nvidia-smi` inside it.

## Reflect (5m)
> What can the old model not express that you'd need at scale (topology, memory, sharing)?

## Resources
- [[NVIDIA GPU Operator Documentation]]
- [[gpu-operator]]
- [[CNCF — KubeCon talks]]

## Tasks
- [ ] Study/open [[NVIDIA GPU Operator Documentation]]
- [ ] Study/open [[gpu-operator]]
- [ ] Study/open [[CNCF — KubeCon talks]]
- [ ] **Build:** On a GPU node (rent one hourly), install the NVIDIA GPU Operator; schedule a GPU pod; confirm with `nvidia-smi` inside it.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
