---
type: "week"
week: 26
phase: "Phase 4 — GPU Orchestration & the AI Platform on Kubernetes"
status: "not-started"
start: 
end: 
objective: "Dynamic Resource Allocation (DRA) — the new substrate (GA in K8s 1.34)."
concepts: ["[[DRA]]"]
project: ["[[Level 4 — AI platform on Kubernetes]]"]
deliverable: 
tags: ["week", "phase/4"]
---

# Week 26 — Dynamic Resource Allocation (DRA)

**Phase:** [[Phase 4 — GPU Orchestration & the AI Platform on Kubernetes]]  
**Objective:** Dynamic Resource Allocation (DRA) — the new substrate (GA in K8s 1.34).  
**Concepts:** [[DRA]]
**Project:** [[Level 4 — AI platform on Kubernetes]]

## Learn (20m)
Kubernetes DRA docs; NVIDIA DRA driver docs; the AWS "DRA for GPUs on EKS" guide.

## Read (15m)
A 2026 DRA + KAI + Grove setup walkthrough.

## Build (20m)
Deploy the NVIDIA DRA driver (Helm) on your cluster; request a GPU via a `ResourceClaimTemplate`; inspect the `ResourceSlice`.

## Reflect (5m)
> How does DRA change capacity planning and multi-tenancy vs the device plugin?

## Resources
- [[Kubernetes DRA Documentation]]
- [[AWS — AI on EKS Guide]]
- [[k8s-dra-driver]]
- [[CNCF — KubeCon talks]]

## Tasks
- [ ] Study/open [[Kubernetes DRA Documentation]]
- [ ] Study/open [[AWS — AI on EKS Guide]]
- [ ] Study/open [[k8s-dra-driver]]
- [ ] Study/open [[CNCF — KubeCon talks]]
- [ ] **Build:** Deploy the NVIDIA DRA driver (Helm) on your cluster; request a GPU via a `ResourceClaimTemplate`; inspect the `ResourceSlice`.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
