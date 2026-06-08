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

## Learn (20m)
PyTorch distributed checkpoint docs; an elastic-training overview (TorchElastic).

## Read (15m)
A frontier-lab writeup on training reliability at scale (stragglers, silent data corruption, fast restart).

## Build (20m)
Add checkpoint/restart to your training job; kill it mid-run and resume; measure restart time.

## Reflect (5m)
> At 1,000 GPUs, what's the business cost of a 30-minute checkpoint interval vs a 5-minute one when a node dies?

## Resources
- [[Meta Engineering & PyTorch Blog]]
- [[PyTorch FSDP]]

## Tasks
- [ ] Study/open [[Meta Engineering & PyTorch Blog]]
- [ ] Study/open [[PyTorch FSDP]]
- [ ] **Build:** Add checkpoint/restart to your training job; kill it mid-run and resume; measure restart time.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
