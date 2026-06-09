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

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
NVIDIA GPU Operator docs; a "GPU scheduling on K8s, the old way" overview.

1. Read the NVIDIA GPU Operator docs.
2. Read a "GPU scheduling on K8s, the old way" overview.
3. Write what the device plugin cannot express (topology, memory, sharing).

## Read (15m)
A 2026 piece on why the device-plugin model is being replaced.

1. Read a 2026 piece on why device-plugin scheduling is ending.
2. Note the limits driving the move to DRA.
3. Write the one capability DRA adds.

## Build (20m)
On a GPU node (rent one hourly), install the NVIDIA GPU Operator; schedule a GPU pod; confirm with `nvidia-smi` inside it.

## Step-by-step
1. Rent a single GPU node hourly with a Kubernetes distro (e.g. k3s/EKS).
2. Install the NVIDIA GPU Operator (Helm) and wait for the device plugin to register GPUs.
3. Schedule a pod requesting `nvidia.com/gpu: 1`; exec in and run `nvidia-smi`.
4. Inspect how the node advertises GPUs and what the device plugin cannot express.

## Reflect (5m)
> What can the old model not express that you'd need at scale (topology, memory, sharing)?

## Done when
- [ ] A GPU pod scheduled and verified with `nvidia-smi` inside it.
- [ ] You can list what the device-plugin model can't express (topology, memory, sharing).
- [ ] You understand why the model is being replaced by DRA.

## Common pitfalls
- Driver/toolkit/operator version mismatches are the #1 cause of GPU pods stuck Pending.
- The device plugin exposes whole GPUs only — no fractional or topology-aware requests.

## Resources
- [[NVIDIA GPU Operator Documentation]]
- [[gpu-operator]]
- [[CNCF — KubeCon talks]]

## Go deeper
- NVIDIA GPU Operator docs.
- A 2026 piece on why the device-plugin model is ending.

## Tasks
- [ ] Study/open [[NVIDIA GPU Operator Documentation]]
- [ ] Study/open [[gpu-operator]]
- [ ] Study/open [[CNCF — KubeCon talks]]
- [ ] **Build:** On a GPU node (rent one hourly), install the NVIDIA GPU Operator; schedule a GPU pod; confirm with `nvidia-smi` inside it.
- [ ] A GPU pod scheduled and verified with `nvidia-smi` inside it.
- [ ] You can list what the device-plugin model can't express (topology, memory, sharing).
- [ ] You understand why the model is being replaced by DRA.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
