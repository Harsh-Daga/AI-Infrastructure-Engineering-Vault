---
type: "week"
week: 7
phase: "Phase 1 — Foundations"
status: "not-started"
start: 
end: 
objective: "Where the GPU time goes: profiling basics — you read kernels, you don't write them."
concepts: ["[[GPU Profiling]]", "[[FlashAttention]]"]
project: ["[[Level 1 — Run local LLMs]]"]
deliverable: 
tags: ["week", "phase/1"]
---

# Week 07 — Where the GPU time goes — profiling

**Phase:** [[Phase 1 — Foundations]]  
**Objective:** Where the GPU time goes: profiling basics — you read kernels, you don't write them.  
**Concepts:** [[GPU Profiling]], [[FlashAttention]]
**Project:** [[Level 1 — Run local LLMs]]

## Learn (20m)
NVIDIA Nsight Systems intro; PyTorch profiler tutorial.

## Read (15m)
Horace He "Brrrr" (finish); a "why your GPU is only 40% utilized" post.

## Build (20m)
Profile a single inference run; identify the biggest time sink (data movement? a kernel? Python overhead?).

## Reflect (5m)
> "GPU at 100% utilization" can still be wasteful — why?

## Resources
- [[Horace He — Making Deep Learning Go Brrrr]]
- [[NVIDIA Deep Learning Institute (DLI)]]
- [[FlashAttention (1 & 2)]]
- [[Horace He & PyTorch Talks]]

## Tasks
- [ ] Study/open [[Horace He — Making Deep Learning Go Brrrr]]
- [ ] Study/open [[NVIDIA Deep Learning Institute (DLI)]]
- [ ] Study/open [[FlashAttention (1 & 2)]]
- [ ] Study/open [[Horace He & PyTorch Talks]]
- [ ] **Build:** Profile a single inference run; identify the biggest time sink (data movement? a kernel? Python overhead?).
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
