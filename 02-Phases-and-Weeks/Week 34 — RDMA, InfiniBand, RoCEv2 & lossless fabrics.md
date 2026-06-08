---
type: "week"
week: 34
phase: "Phase 5 — Networking, Distributed Systems for AI, Distributed Training"
status: "not-started"
start: 
end: 
objective: "★ RDMA, InfiniBand, RoCEv2 & lossless fabrics: verbs, kernel bypass, PFC/ECN, congestion control."
concepts: ["[[RDMA]]", "[[InfiniBand vs RoCE]]"]
project: []
deliverable: 
tags: ["week", "phase/5"]
---

# Week 34 — RDMA, InfiniBand, RoCEv2 & lossless fabrics

**Phase:** [[Phase 5 — Networking, Distributed Systems for AI, Distributed Training]]  
**Objective:** ★ RDMA, InfiniBand, RoCEv2 & lossless fabrics: verbs, kernel bypass, PFC/ECN, congestion control.  
**Concepts:** [[RDMA]], [[InfiniBand vs RoCE]]

## Learn (20m)
An RDMA fundamentals course/intro; InfiniBand vs RoCE comparison.

## Read (15m)
A hyperscaler AI-fabric writeup (e.g. Meta's RoCE-for-AI engineering posts).

## Build (20m)
If you can access RDMA-capable nodes, run `ib_write_bw`/`perftest`; otherwise study real fabric topologies and draw a rail-optimized cluster diagram.

## Reflect (5m)
> Why does the network, not the GPU, often determine how large a training run can scale?

## Resources
- [[Meta Engineering & PyTorch Blog]]
- [[SemiAnalysis]]
- [[NVIDIA Deep Learning Institute (DLI)]]

## Tasks
- [ ] Study/open [[Meta Engineering & PyTorch Blog]]
- [ ] Study/open [[SemiAnalysis]]
- [ ] Study/open [[NVIDIA Deep Learning Institute (DLI)]]
- [ ] **Build:** If you can access RDMA-capable nodes, run `ib_write_bw`/`perftest`; otherwise study real fabric topologies and draw a rail-optimized cluster diagram.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
