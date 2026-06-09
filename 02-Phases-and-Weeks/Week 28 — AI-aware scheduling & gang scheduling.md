---
type: "week"
week: 28
phase: "Phase 4 — GPU Orchestration & the AI Platform on Kubernetes"
status: "not-started"
start: 
end: 
objective: "AI-aware scheduling: KAI, Kueue, Volcano, gang scheduling, priority/preemption, fair share."
concepts: ["[[Gang Scheduling]]"]
project: ["[[Level 4 — AI platform on Kubernetes]]", "[[Level 5 — GPU scheduling deep-dive]]"]
deliverable: 
tags: ["week", "phase/4"]
---

# Week 28 — AI-aware scheduling & gang scheduling

**Phase:** [[Phase 4 — GPU Orchestration & the AI Platform on Kubernetes]]  
**Objective:** AI-aware scheduling: KAI, Kueue, Volcano, gang scheduling, priority/preemption, fair share.  
**Concepts:** [[Gang Scheduling]]
**Project:** [[Level 4 — AI platform on Kubernetes]], [[Level 5 — GPU scheduling deep-dive]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
KAI Scheduler docs; Kueue docs; Volcano overview.

## Read (15m)
A "multi-tenant GPU scheduling" engineering post.

## Build (20m)
Install KAI or Volcano; submit a multi-pod "gang" job that only runs when all pods can be placed; observe preemption with priorities.

## Step-by-step
1. Install KAI Scheduler (or Volcano) on your cluster.
2. Define queues with priorities and fair-share weights.
3. Submit a multi-pod "gang" job that only starts when all pods can be placed.
4. Submit a higher-priority job and observe preemption of the lower-priority one.
5. Note what happens to a gang job when even one pod can't be scheduled.

## Reflect (5m)
> Why does a distributed training job require gang scheduling, and what happens without it?

## Done when
- [ ] A gang job that runs all-or-nothing.
- [ ] Observed preemption driven by priority.
- [ ] You can explain why distributed training needs gang scheduling.

## Common pitfalls
- Without gang scheduling, a partially-placed distributed job deadlocks holding GPUs idle.
- Aggressive preemption without checkpointing throws away work — pair them.

## Resources
- [[KAI-Scheduler]]
- [[volcano]]
- [[kueue]]
- [[CNCF — KubeCon talks]]

## Go deeper
- KAI Scheduler / Kueue / Volcano docs.
- A "multi-tenant GPU scheduling" engineering post.

## Tasks
- [ ] Study/open [[KAI-Scheduler]]
- [ ] Study/open [[volcano]]
- [ ] Study/open [[kueue]]
- [ ] Study/open [[CNCF — KubeCon talks]]
- [ ] **Build:** Install KAI or Volcano; submit a multi-pod "gang" job that only runs when all pods can be placed; observe preemption with priorities.
- [ ] A gang job that runs all-or-nothing.
- [ ] Observed preemption driven by priority.
- [ ] You can explain why distributed training needs gang scheduling.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
