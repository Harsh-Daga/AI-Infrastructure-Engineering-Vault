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

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
Kubernetes DRA docs; NVIDIA DRA driver docs; the AWS "DRA for GPUs on EKS" guide.

1. Read Kubernetes DRA docs + the NVIDIA DRA driver docs.
2. Skim the AWS "DRA for GPUs on EKS" guide.
3. Write the new objects: DeviceClass, ResourceClaim, ResourceSlice.

## Read (15m)
A 2026 DRA + KAI + Grove setup walkthrough.

1. Read a 2026 DRA + KAI + Grove walkthrough.
2. Note how DRA changes multi-tenancy.
3. Write the version requirement (DRA GA in K8s 1.34).

## Build (20m)
Deploy the NVIDIA DRA driver (Helm) on your cluster; request a GPU via a `ResourceClaimTemplate`; inspect the `ResourceSlice`.

## Step-by-step
1. On your cluster, install the NVIDIA DRA driver via Helm.
2. Define a `DeviceClass` and request a GPU through a `ResourceClaimTemplate`.
3. Deploy a pod that consumes the claim; confirm it gets the GPU.
4. Inspect the resulting `ResourceClaim` and `ResourceSlice` objects to see the new model.
5. Contrast capacity planning and multi-tenancy under DRA vs the device plugin.

## Reflect (5m)
> How does DRA change capacity planning and multi-tenancy vs the device plugin?

## Done when
- [ ] A GPU successfully requested and consumed via a ResourceClaim.
- [ ] You inspected ResourceSlice/ResourceClaim and can explain them.
- [ ] You can articulate how DRA changes multi-tenancy.

## Common pitfalls
- DRA needs a recent Kubernetes (GA in 1.34) and the matching driver — check versions first.
- Claim templates vs shared claims behave differently; pick deliberately for multi-tenancy.

## Resources
- [[Kubernetes DRA Documentation]]
- [[AWS — AI on EKS Guide]]
- [[k8s-dra-driver]]
- [[CNCF — KubeCon talks]]

## Go deeper
- Kubernetes DRA docs + NVIDIA DRA driver docs.
- The AWS "DRA for GPUs on EKS" guide; a KAI + Grove walkthrough.

## Tasks
- [ ] Study/open [[Kubernetes DRA Documentation]]
- [ ] Study/open [[AWS — AI on EKS Guide]]
- [ ] Study/open [[k8s-dra-driver]]
- [ ] Study/open [[CNCF — KubeCon talks]]
- [ ] **Build:** Deploy the NVIDIA DRA driver (Helm) on your cluster; request a GPU via a `ResourceClaimTemplate`; inspect the `ResourceSlice`.
- [ ] A GPU successfully requested and consumed via a ResourceClaim.
- [ ] You inspected ResourceSlice/ResourceClaim and can explain them.
- [ ] You can articulate how DRA changes multi-tenancy.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
