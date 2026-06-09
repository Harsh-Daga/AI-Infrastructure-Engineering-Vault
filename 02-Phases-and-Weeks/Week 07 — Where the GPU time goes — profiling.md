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

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
NVIDIA Nsight Systems intro; PyTorch profiler tutorial.

## Read (15m)
Horace He "Brrrr" (finish); a "why your GPU is only 40% utilized" post.

## Build (20m)
Profile a single inference run; identify the biggest time sink (data movement? a kernel? Python overhead?).

## Step-by-step
1. Install Nsight Systems (or use the PyTorch profiler) and capture one inference run.
2. Open the timeline; identify the single biggest time sink (kernel, data movement, or Python overhead).
3. Look for gaps between kernels (host-side stalls) and small back-to-back kernels (launch overhead).
4. Write down the top-3 time consumers and one hypothesis to reduce each.

## Reflect (5m)
> "GPU at 100% utilization" can still be wasteful — why?

## Done when
- [ ] You produced a profile/timeline of a real inference run.
- [ ] You named the dominant time sink with evidence from the trace.
- [ ] You can explain why 100% GPU-util can still be wasteful.

## Common pitfalls
- Profiling the first iteration captures warmup/compile noise — profile a steady-state step.
- CPU-side Python overhead is invisible in nvidia-smi but obvious in a timeline.

## Resources
- [[Horace He — Making Deep Learning Go Brrrr]]
- [[NVIDIA Deep Learning Institute (DLI)]]
- [[FlashAttention (1 & 2)]]
- [[Horace He & PyTorch Talks]]

## Go deeper
- NVIDIA Nsight Systems getting-started guide.
- FlashAttention paper — why fusing the attention kernel removes HBM round-trips.

## Tasks
- [ ] Study/open [[Horace He — Making Deep Learning Go Brrrr]]
- [ ] Study/open [[NVIDIA Deep Learning Institute (DLI)]]
- [ ] Study/open [[FlashAttention (1 & 2)]]
- [ ] Study/open [[Horace He & PyTorch Talks]]
- [ ] **Build:** Profile a single inference run; identify the biggest time sink (data movement? a kernel? Python overhead?).
- [ ] You produced a profile/timeline of a real inference run.
- [ ] You named the dominant time sink with evidence from the trace.
- [ ] You can explain why 100% GPU-util can still be wasteful.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
