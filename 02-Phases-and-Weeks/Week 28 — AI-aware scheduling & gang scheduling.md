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

## Learn (20m)
KAI Scheduler docs; Kueue docs; Volcano overview.

## Read (15m)
A "multi-tenant GPU scheduling" engineering post.

## Build (20m)
Install KAI or Volcano; submit a multi-pod "gang" job that only runs when all pods can be placed; observe preemption with priorities.

## Reflect (5m)
> Why does a distributed training job require gang scheduling, and what happens without it?

## Resources
- [[KAI-Scheduler]]
- [[volcano]]
- [[kueue]]
- [[CNCF — KubeCon talks]]

## Tasks
- [ ] Study/open [[KAI-Scheduler]]
- [ ] Study/open [[volcano]]
- [ ] Study/open [[kueue]]
- [ ] Study/open [[CNCF — KubeCon talks]]
- [ ] **Build:** Install KAI or Volcano; submit a multi-pod "gang" job that only runs when all pods can be placed; observe preemption with priorities.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
