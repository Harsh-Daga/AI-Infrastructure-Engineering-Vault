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

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
NVIDIA NCCL docs; a "collective communication explained" talk.

## Read (15m)
The ring/tree all-reduce explainer; NCCL tuning notes.

## Build (20m)
Run NCCL tests (`nccl-tests`) on a multi-GPU node; measure all-reduce bandwidth; compare with theoretical NVLink BW.

## Step-by-step
1. On a multi-GPU node, build and run `nccl-tests` (e.g. `all_reduce_perf`).
2. Sweep message sizes; record bus bandwidth and compare to theoretical NVLink BW.
3. Repeat for all-gather and reduce-scatter; note how each scales.
4. Map each collective to where it appears in data-parallel training (gradient all-reduce).

## Reflect (5m)
> Why is all-reduce the operation that dominates data-parallel training time at scale?

## Done when
- [ ] An all-reduce bandwidth curve vs message size, compared to NVLink theoretical.
- [ ] You can describe ring vs tree all-reduce and when each wins.
- [ ] You can explain why all-reduce dominates data-parallel training time at scale.

## Common pitfalls
- Small messages are latency-bound, not bandwidth-bound — the curve has two regimes.
- `NCCL_DEBUG=INFO` reveals the chosen algorithm/topology; mismatches explain bad numbers.

## Resources
- [[nccl]]
- [[nccl-tests]]
- [[NVIDIA Deep Learning Institute (DLI)]]
- [[Hugging Face Ultra-Scale Playbook]]

## Go deeper
- NVIDIA NCCL docs + the ring/tree all-reduce explainer.
- Hugging Face Ultra-Scale Playbook — collectives in context.

## Tasks
- [ ] Study/open [[nccl]]
- [ ] Study/open [[nccl-tests]]
- [ ] Study/open [[NVIDIA Deep Learning Institute (DLI)]]
- [ ] Study/open [[Hugging Face Ultra-Scale Playbook]]
- [ ] **Build:** Run NCCL tests (`nccl-tests`) on a multi-GPU node; measure all-reduce bandwidth; compare with theoretical NVLink BW.
- [ ] An all-reduce bandwidth curve vs message size, compared to NVLink theoretical.
- [ ] You can describe ring vs tree all-reduce and when each wins.
- [ ] You can explain why all-reduce dominates data-parallel training time at scale.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
