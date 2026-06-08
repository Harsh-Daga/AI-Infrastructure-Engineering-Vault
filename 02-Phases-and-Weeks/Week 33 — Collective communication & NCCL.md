---
type: "week"
week: 33
phase: "Phase 5 — Networking, Distributed Systems for AI, Distributed Training"
status: "not-started"
start: 
end: 
objective: "★ Collective communication & NCCL: all-reduce, all-gather, reduce-scatter; the bridge concept."
concepts: ["[[Collective Communication (NCCL)]]"]
project: []
deliverable: 
tags: ["week", "phase/5"]
---

# Week 33 — Collective communication & NCCL

**Phase:** [[Phase 5 — Networking, Distributed Systems for AI, Distributed Training]]  
**Objective:** ★ Collective communication & NCCL: all-reduce, all-gather, reduce-scatter; the bridge concept.  
**Concepts:** [[Collective Communication (NCCL)]]

## Learn (20m)
NVIDIA NCCL docs; a "collective communication explained" talk.

## Read (15m)
The ring/tree all-reduce explainer; NCCL tuning notes.

## Build (20m)
Run NCCL tests (`nccl-tests`) on a multi-GPU node; measure all-reduce bandwidth; compare with theoretical NVLink BW.

## Reflect (5m)
> Why is all-reduce the operation that dominates data-parallel training time at scale?

## Resources
- [[nccl]]
- [[nccl-tests]]
- [[NVIDIA Deep Learning Institute (DLI)]]
- [[Hugging Face Ultra-Scale Playbook]]

## Tasks
- [ ] Study/open [[nccl]]
- [ ] Study/open [[nccl-tests]]
- [ ] Study/open [[NVIDIA Deep Learning Institute (DLI)]]
- [ ] Study/open [[Hugging Face Ultra-Scale Playbook]]
- [ ] **Build:** Run NCCL tests (`nccl-tests`) on a multi-GPU node; measure all-reduce bandwidth; compare with theoretical NVLink BW.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
