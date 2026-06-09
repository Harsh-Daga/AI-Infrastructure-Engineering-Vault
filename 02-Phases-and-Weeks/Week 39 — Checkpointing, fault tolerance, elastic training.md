---
type: "week"
week: 39
phase: "Phase 5 — Networking, Distributed Systems for AI, Distributed Training"
status: "not-started"
start: 
end: 
objective: "Checkpointing, fault tolerance, elastic training: distributed/async checkpointing, restart, stragglers."
concepts: ["[[Checkpointing and Fault Tolerance]]"]
project: []
deliverable: 
tags: ["week", "phase/5"]
---

# Week 39 — Checkpointing, fault tolerance, elastic training

**Phase:** [[Phase 5 — Networking, Distributed Systems for AI, Distributed Training]]  
**Objective:** Checkpointing, fault tolerance, elastic training: distributed/async checkpointing, restart, stragglers.  
**Concepts:** [[Checkpointing and Fault Tolerance]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
PyTorch distributed checkpoint docs; an elastic-training overview (TorchElastic).

1. Read PyTorch distributed checkpoint docs.
2. Read a TorchElastic elastic-training overview.
3. Write the sync vs async/sharded checkpointing tradeoff.

## Read (15m)
A frontier-lab writeup on training reliability at scale (stragglers, silent data corruption, fast restart).

1. Read a frontier-lab training-reliability writeup.
2. Note their checkpoint interval and restart strategy.
3. Write the cost of a node death at their scale.

## Build (20m)
Add checkpoint/restart to your training job; kill it mid-run and resume; measure restart time.

## Step-by-step
1. Add distributed checkpoint save/load (PyTorch DCP) to your training job.
2. Kill the job mid-run; resume from the last checkpoint and verify loss continuity.
3. Measure checkpoint write time and restart-to-productive time.
4. Compute the cost of a 30-min vs 5-min checkpoint interval at 1,000 GPUs when a node dies.

## Reflect (5m)
> At 1,000 GPUs, what's the business cost of a 30-minute checkpoint interval vs a 5-minute one when a node dies?

## Done when
- [ ] A job that checkpoints, is killed, and resumes correctly.
- [ ] Measured restart time and checkpoint overhead.
- [ ] A back-of-envelope cost model for checkpoint interval at scale.

## Common pitfalls
- Synchronous checkpointing stalls all GPUs — use async/sharded checkpointing at scale.
- Resuming with a different world size needs elastic/resharding support, or it fails.

## Resources
- [[Meta Engineering & PyTorch Blog]]
- [[PyTorch FSDP]]

## Go deeper
- PyTorch distributed checkpoint docs; TorchElastic overview.
- A frontier-lab training-reliability writeup (stragglers, SDC, fast restart).

## Tasks
- [ ] Study/open [[Meta Engineering & PyTorch Blog]]
- [ ] Study/open [[PyTorch FSDP]]
- [ ] **Build:** Add checkpoint/restart to your training job; kill it mid-run and resume; measure restart time.
- [ ] A job that checkpoints, is killed, and resumes correctly.
- [ ] Measured restart time and checkpoint overhead.
- [ ] A back-of-envelope cost model for checkpoint interval at scale.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
