---
type: "project"
level: 5
status: "not-started"
phase: "[[Phase 4 — GPU Orchestration & the AI Platform on Kubernetes]]"
skills: ["[[Gang Scheduling]]", "[[GPU Sharing (MIG and MPS)]]", "[[Cluster Topology]]", "[[DRA]]"]
repos: ["[[KAI-Scheduler]]", "[[volcano]]", "[[kueue]]"]
success-criteria: "Show sustained GPU utilization improvement (e.g. 60%→85%) under a mixed workload, with training jobs gang-scheduled and inference preempting on priority correctly."
tags: ["project", "level/5"]
---

# Level 5 — GPU scheduling deep-dive

**Phase:** [[Phase 4 — GPU Orchestration & the AI Platform on Kubernetes]]  
**Weeks:** [[Week 27 — GPU sharing — MIG, MPS, time-slicing]], [[Week 28 — AI-aware scheduling & gang scheduling]]

## Architecture
A multi-tenant GPU cluster running training, batch, and online inference in shared pools with gang scheduling, priority/preemption, MIG partitioning, and topology awareness.

## Components
KAI/Volcano with queues and quotas, MIG profiles, priority classes, topology-aware placement.

## Why it matters
Co-scheduling heterogeneous workloads on one expensive fleet is an unsolved-in-practice, high-comp problem.

## Skills learned
gang scheduling, preemption, fair share, MIG economics, topology-aware placement.

## Skills (concept links)

- [[Gang Scheduling]]
- [[GPU Sharing (MIG and MPS)]]
- [[Cluster Topology]]
- [[DRA]]

## Success criteria
> Show sustained GPU utilization improvement (e.g. 60%→85%) under a mixed workload, with training jobs gang-scheduled and inference preempting on priority correctly.

## Repos to study
[[KAI-Scheduler]], [[volcano]], [[kueue]]

## Build log
_Log progress here as you build._


## Tasks
- [ ] Scaffold the repo with a real README and architecture doc
- [ ] Implement the core architecture above
- [ ] Produce the benchmark / cost model that proves the success criteria
- [ ] Write the "what I learned" section and publish to the learning log
