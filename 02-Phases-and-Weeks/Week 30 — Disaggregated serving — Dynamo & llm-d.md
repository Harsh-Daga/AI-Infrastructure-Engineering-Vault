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

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
NVIDIA Dynamo docs (architecture + disaggregation); llm-d docs.

## Read (15m)
"NVIDIA Dynamo: productionizing disaggregated inference" + the K8s operator design.

## Build (20m)
Deploy Dynamo (or llm-d) with separate prefill and decode workers on a multi-GPU node; trace a request through both pools.

## Step-by-step
1. On a multi-GPU node, deploy NVIDIA Dynamo (or llm-d) with separate prefill and decode workers.
2. Configure KV-aware routing so decode reuses prefill's KV via the transfer layer (NIXL).
3. Send a request and trace it through the prefill pool then the decode pool.
4. Measure KV-transfer overhead and compare end-to-end latency vs aggregated serving.
5. Enumerate the new failure modes introduced by the split.

## Reflect (5m)
> What new failure modes appear once prefill and decode are separate services connected by RDMA?

## Done when
- [ ] A request traced through separate prefill and decode pools.
- [ ] Measured KV-transfer overhead vs aggregated serving.
- [ ] A list of new failure modes (RDMA hiccups, pool imbalance, routing staleness).

## Common pitfalls
- Prefill/decode pool ratio must match your workload, or one pool starves the other.
- KV transfer over the fabric adds latency and a new dependency that can fail independently.

## Resources
- [[NVIDIA Dynamo Documentation]]
- [[dynamo]]
- [[llm-d]]
- [[NVIDIA Technical Blog]]

## Go deeper
- NVIDIA Dynamo docs (architecture + disaggregation); llm-d docs.
- "Productionizing disaggregated inference" + the K8s operator design.

## Tasks
- [ ] Study/open [[NVIDIA Dynamo Documentation]]
- [ ] Study/open [[dynamo]]
- [ ] Study/open [[llm-d]]
- [ ] Study/open [[NVIDIA Technical Blog]]
- [ ] **Build:** Deploy Dynamo (or llm-d) with separate prefill and decode workers on a multi-GPU node; trace a request through both pools.
- [ ] A request traced through separate prefill and decode pools.
- [ ] Measured KV-transfer overhead vs aggregated serving.
- [ ] A list of new failure modes (RDMA hiccups, pool imbalance, routing staleness).
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
