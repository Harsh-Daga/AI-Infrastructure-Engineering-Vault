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

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
An RDMA fundamentals course/intro; InfiniBand vs RoCE comparison.

1. Work through an RDMA fundamentals intro.
2. Read an InfiniBand vs RoCE comparison.
3. Write the lossless mechanisms (PFC/ECN) and why they matter.

## Read (15m)
A hyperscaler AI-fabric writeup (e.g. Meta's RoCE-for-AI engineering posts).

1. Read a hyperscaler AI-fabric writeup (e.g. Meta's RoCE-for-AI posts).
2. Note their congestion-control choices.
3. Write why the network caps training scale.

## Build (20m)
If you can access RDMA-capable nodes, run `ib_write_bw`/`perftest`; otherwise study real fabric topologies and draw a rail-optimized cluster diagram.

## Step-by-step
1. If you have RDMA-capable nodes, run `perftest` (`ib_write_bw`/`ib_read_bw`) and record bandwidth/latency.
2. Inspect the fabric: `ibstat`, ` show_gids`, and the InfiniBand vs RoCE config differences.
3. If no RDMA access, study a published AI-fabric topology and draw a rail-optimized cluster diagram.
4. Annotate where PFC/ECN and congestion control matter for lossless operation.

## Reflect (5m)
> Why does the network, not the GPU, often determine how large a training run can scale?

## Done when
- [ ] An RDMA bandwidth/latency measurement, or a detailed rail-optimized topology diagram.
- [ ] You can contrast InfiniBand vs RoCEv2 (lossless mechanisms, ops burden).
- [ ] You can explain why the network often caps training scale, not the GPU.

## Common pitfalls
- RoCEv2 needs correctly configured PFC/ECN end-to-end or you get drops and collapse.
- Kernel-bypass (verbs) means standard network tools won't see the traffic.

## Resources
- [[Meta Engineering & PyTorch Blog]]
- [[SemiAnalysis]]
- [[NVIDIA Deep Learning Institute (DLI)]]

## Go deeper
- An RDMA fundamentals intro; InfiniBand vs RoCE comparison.
- A hyperscaler AI-fabric writeup (e.g. Meta's RoCE-for-AI posts).

## Tasks
- [ ] Study/open [[Meta Engineering & PyTorch Blog]]
- [ ] Study/open [[SemiAnalysis]]
- [ ] Study/open [[NVIDIA Deep Learning Institute (DLI)]]
- [ ] **Build:** If you can access RDMA-capable nodes, run `ib_write_bw`/`perftest`; otherwise study real fabric topologies and draw a rail-optimized cluster diagram.
- [ ] An RDMA bandwidth/latency measurement, or a detailed rail-optimized topology diagram.
- [ ] You can contrast InfiniBand vs RoCEv2 (lossless mechanisms, ops burden).
- [ ] You can explain why the network often caps training scale, not the GPU.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
