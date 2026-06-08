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

## Learn (20m)
Dynamo multi-node disaggregation docs; SGLang/vLLM multi-node serving.

## Read (15m)
A "serving a frontier-size model" architecture writeup.

## Build (20m)
Stand up a 2-node disaggregated inference cluster (rent hourly); route a request across nodes; measure KV-transfer overhead.

## Reflect (5m)
> As you add nodes, what becomes the bottleneck — GPU, fabric, routing, or coordination?

## Resources
- [[NVIDIA Dynamo Documentation]]
- [[dynamo]]
- [[sglang]]
- [[vllm]]

## Tasks
- [ ] Study/open [[NVIDIA Dynamo Documentation]]
- [ ] Study/open [[dynamo]]
- [ ] Study/open [[sglang]]
- [ ] Study/open [[vllm]]
- [ ] **Build:** Stand up a 2-node disaggregated inference cluster (rent hourly); route a request across nodes; measure KV-transfer overhead.
- [ ] **Reflect:** answer the week's question in the learning log

## Phase deliverable
> [!success] Phase-5 deliverable: a documented distributed inference cluster + a training-reliability runbook (Project Levels 5–6).

## Notes
