---
type: "week"
week: 14
phase: "Phase 2 — LLM Serving, Deep"
status: "not-started"
start: 
end: 
objective: "Serving metrics, SLOs & load testing done right: TTFT, ITL/TBT, goodput, p50/p95/p99."
concepts: ["[[TTFT vs ITL]]"]
project: []
deliverable: 
tags: ["week", "phase/2"]
---

# Week 14 — Serving metrics, SLOs & load testing

**Phase:** [[Phase 2 — LLM Serving, Deep]]  
**Objective:** Serving metrics, SLOs & load testing done right: TTFT, ITL/TBT, goodput, p50/p95/p99.  
**Concepts:** [[TTFT vs ITL]]

## Learn (20m)
Read about LLM-specific SLOs (TTFT and inter-token latency as separate SLOs).

## Read (15m)
A production "how we set LLM SLOs" engineering post.

## Build (20m)
Add Prometheus + Grafana to your vLLM deployment; build a dashboard with TTFT, ITL, throughput, queue depth, KV utilization.

## Reflect (5m)
> Which metric best predicts user-perceived quality, and why isn't it average latency?

## Resources
- [[vLLM Documentation]]
- [[Grafana Labs & Red Hat (OpenShift AI)]]

## Tasks
- [ ] Study/open [[vLLM Documentation]]
- [ ] Study/open [[Grafana Labs & Red Hat (OpenShift AI)]]
- [ ] **Build:** Add Prometheus + Grafana to your vLLM deployment; build a dashboard with TTFT, ITL, throughput, queue depth, KV utilization.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
