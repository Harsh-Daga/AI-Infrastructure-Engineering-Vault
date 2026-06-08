---
type: "week"
week: 40
phase: "Phase 5 — Networking, Distributed Systems for AI, Distributed Training"
status: "not-started"
start: 
end: 
objective: "Silent failures, stragglers & training reliability engineering: SDC, slow-node detection, NCCL hangs."
concepts: ["[[Stragglers and SDC]]", "[[AI Reliability Engineering]]"]
project: []
deliverable: 
tags: ["week", "phase/5"]
---

# Week 40 — Silent failures, stragglers & reliability

**Phase:** [[Phase 5 — Networking, Distributed Systems for AI, Distributed Training]]  
**Objective:** Silent failures, stragglers & training reliability engineering: SDC, slow-node detection, NCCL hangs.  
**Concepts:** [[Stragglers and SDC]], [[AI Reliability Engineering]]

## Learn (20m)
NCCL debugging guides; a "debugging a distributed training hang" talk.

## Read (15m)
Public postmortems / writeups on training-cluster reliability.

## Build (20m)
Write a pre-flight cluster health check script (GPU health, NCCL all-reduce sanity, fabric bandwidth) you'd run before a big job.

## Reflect (5m)
> A run is 20% slower than expected with no errors. Walk through your diagnostic tree.

## Resources
- [[nccl]]
- [[Meta Engineering & PyTorch Blog]]
- [[Uber, Netflix & Stripe Engineering]]

## Tasks
- [ ] Study/open [[nccl]]
- [ ] Study/open [[Meta Engineering & PyTorch Blog]]
- [ ] Study/open [[Uber, Netflix & Stripe Engineering]]
- [ ] **Build:** Write a pre-flight cluster health check script (GPU health, NCCL all-reduce sanity, fabric bandwidth) you'd run before a big job.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
