---
type: "week"
week: 30
phase: "Phase 4 — GPU Orchestration & the AI Platform on Kubernetes"
status: "not-started"
start: 
end: 
objective: "Disaggregated serving on Kubernetes: Dynamo & llm-d, prefill/decode pools, KV-aware routing, NIXL."
concepts: ["[[Disaggregated Serving]]", "[[KV Routing]]", "[[Inference Autoscaling]]"]
project: ["[[Level 4 — AI platform on Kubernetes]]", "[[Level 6 — Distributed inference cluster]]"]
deliverable: 
tags: ["week", "phase/4"]
---

# Week 30 — Disaggregated serving — Dynamo & llm-d

**Phase:** [[Phase 4 — GPU Orchestration & the AI Platform on Kubernetes]]  
**Objective:** Disaggregated serving on Kubernetes: Dynamo & llm-d, prefill/decode pools, KV-aware routing, NIXL.  
**Concepts:** [[Disaggregated Serving]], [[KV Routing]], [[Inference Autoscaling]]
**Project:** [[Level 4 — AI platform on Kubernetes]], [[Level 6 — Distributed inference cluster]]

## Learn (20m)
NVIDIA Dynamo docs (architecture + disaggregation); llm-d docs.

## Read (15m)
"NVIDIA Dynamo: productionizing disaggregated inference" + the K8s operator design.

## Build (20m)
Deploy Dynamo (or llm-d) with separate prefill and decode workers on a multi-GPU node; trace a request through both pools.

## Reflect (5m)
> What new failure modes appear once prefill and decode are separate services connected by RDMA?

## Resources
- [[NVIDIA Dynamo Documentation]]
- [[dynamo]]
- [[llm-d]]
- [[NVIDIA Technical Blog]]

## Tasks
- [ ] Study/open [[NVIDIA Dynamo Documentation]]
- [ ] Study/open [[dynamo]]
- [ ] Study/open [[llm-d]]
- [ ] Study/open [[NVIDIA Technical Blog]]
- [ ] **Build:** Deploy Dynamo (or llm-d) with separate prefill and decode workers on a multi-GPU node; trace a request through both pools.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
