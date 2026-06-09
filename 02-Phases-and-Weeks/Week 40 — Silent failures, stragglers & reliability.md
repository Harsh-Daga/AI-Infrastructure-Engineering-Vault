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

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
NCCL debugging guides; a "debugging a distributed training hang" talk.

## Read (15m)
Public postmortems / writeups on training-cluster reliability.

## Build (20m)
Write a pre-flight cluster health check script (GPU health, NCCL all-reduce sanity, fabric bandwidth) you'd run before a big job.

## Step-by-step
1. Write a pre-flight cluster health check: per-GPU health (DCGM), NCCL all-reduce sanity, fabric BW.
2. Run it on a node and intentionally degrade one GPU (power-cap/throttle) to see it flagged.
3. Build a diagnostic decision tree for "run is 20% slow, no errors."
4. Document NCCL-hang debugging steps (`NCCL_DEBUG`, timeouts, watchdog).

## Reflect (5m)
> A run is 20% slower than expected with no errors. Walk through your diagnostic tree.

## Done when
- [ ] A reusable pre-flight health-check script.
- [ ] A written diagnostic tree for a silent slowdown.
- [ ] You can explain straggler detection and SDC, and why they're insidious.

## Common pitfalls
- Silent data corruption produces no error — only divergent results; you need cross-checks to catch it.
- One slow straggler drags the whole synchronous job to its speed; find it via per-rank timing.

## Resources
- [[nccl]]
- [[Meta Engineering & PyTorch Blog]]
- [[Uber, Netflix & Stripe Engineering]]

## Go deeper
- NCCL debugging guides; a "debugging a distributed training hang" talk.
- Public postmortems on training-cluster reliability.

## Tasks
- [ ] Study/open [[nccl]]
- [ ] Study/open [[Meta Engineering & PyTorch Blog]]
- [ ] Study/open [[Uber, Netflix & Stripe Engineering]]
- [ ] **Build:** Write a pre-flight cluster health check script (GPU health, NCCL all-reduce sanity, fabric bandwidth) you'd run before a big job.
- [ ] A reusable pre-flight health-check script.
- [ ] A written diagnostic tree for a silent slowdown.
- [ ] You can explain straggler detection and SDC, and why they're insidious.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
