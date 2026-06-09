---
type: "week"
week: 42
phase: "Phase 5 — Networking, Distributed Systems for AI, Distributed Training"
status: "not-started"
start: 
end: 
objective: "Distributed inference at scale (tying it together): cross-node serving, KV transfer over fabric, global routing."
concepts: ["[[Disaggregated Serving]]", "[[KV Routing]]", "[[KV Offload]]", "[[Cluster Topology]]"]
project: ["[[Level 6 — Distributed inference cluster]]"]
deliverable: "Phase-5 deliverable: a documented distributed inference cluster + a training-reliability runbook (Project Levels 5–6)."
tags: ["week", "phase/5"]
---

# Week 42 — Distributed inference at scale

**Phase:** [[Phase 5 — Networking, Distributed Systems for AI, Distributed Training]]  
**Objective:** Distributed inference at scale (tying it together): cross-node serving, KV transfer over fabric, global routing.  
**Concepts:** [[Disaggregated Serving]], [[KV Routing]], [[KV Offload]], [[Cluster Topology]]
**Project:** [[Level 6 — Distributed inference cluster]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
Dynamo multi-node disaggregation docs; SGLang/vLLM multi-node serving.

## Read (15m)
A "serving a frontier-size model" architecture writeup.

## Build (20m)
Stand up a 2-node disaggregated inference cluster (rent hourly); route a request across nodes; measure KV-transfer overhead.

## Step-by-step
1. Rent a 2-node multi-GPU setup hourly with RDMA if possible.
2. Stand up disaggregated inference (Dynamo/llm-d) across both nodes.
3. Route a request across nodes; measure KV-transfer overhead over the fabric.
4. Scale from 1→2 nodes and identify what becomes the bottleneck (GPU/fabric/routing/coordination).
5. Update the Phase-5 deliverable: distributed inference cluster + reliability runbook.

## Reflect (5m)
> As you add nodes, what becomes the bottleneck — GPU, fabric, routing, or coordination?

## Done when
- [ ] A 2-node disaggregated inference cluster routing requests across nodes.
- [ ] Measured cross-node KV-transfer overhead.
- [ ] Phase-5 deliverable assembled (Project Levels 5–6).

## Common pitfalls
- Cross-node KV transfer needs fast fabric; over plain TCP it dominates and disaggregation loses.
- Global routing becomes the new bottleneck before GPUs do — instrument it.

## Resources
- [[NVIDIA Dynamo Documentation]]
- [[dynamo]]
- [[sglang]]
- [[vllm]]

## Go deeper
- Dynamo multi-node disaggregation docs; SGLang/vLLM multi-node serving.
- A "serving a frontier-size model" architecture writeup.

## Tasks
- [ ] Study/open [[NVIDIA Dynamo Documentation]]
- [ ] Study/open [[dynamo]]
- [ ] Study/open [[sglang]]
- [ ] Study/open [[vllm]]
- [ ] **Build:** Stand up a 2-node disaggregated inference cluster (rent hourly); route a request across nodes; measure KV-transfer overhead.
- [ ] A 2-node disaggregated inference cluster routing requests across nodes.
- [ ] Measured cross-node KV-transfer overhead.
- [ ] Phase-5 deliverable assembled (Project Levels 5–6).
- [ ] **Reflect:** answer the week's question in the learning log

## Phase deliverable
> [!success] Phase-5 deliverable: a documented distributed inference cluster + a training-reliability runbook (Project Levels 5–6).

## Notes
