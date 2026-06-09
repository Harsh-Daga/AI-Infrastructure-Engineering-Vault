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

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
Read about LLM-specific SLOs (TTFT and inter-token latency as separate SLOs).

1. Read about LLM-specific SLOs: TTFT and inter-token latency as separate SLOs.
2. Learn the metric definitions: TTFT, ITL/TBT, goodput, p50/p95/p99.
3. Write why average latency is the wrong headline metric.

## Read (15m)
A production "how we set LLM SLOs" engineering post.

1. Read a production "how we set LLM SLOs" post.
2. Note which percentile they alert on and why.
3. Write their TTFT and ITL targets as a reference point.

## Build (20m)
Add Prometheus + Grafana to your vLLM deployment; build a dashboard with TTFT, ITL, throughput, queue depth, KV utilization.

## Step-by-step
1. Add the Prometheus metrics endpoint to your vLLM deployment.
2. Stand up Prometheus + Grafana (docker-compose is fine) and scrape the endpoint.
3. Build a dashboard: TTFT, ITL/TBT, throughput, queue depth, KV-cache utilization (p50/p95/p99).
4. Run a load test and watch which panel moves first as you approach saturation.
5. Write down candidate SLOs (e.g. p95 TTFT < X, p95 ITL < Y) for your workload.

## Reflect (5m)
> Which metric best predicts user-perceived quality, and why isn't it average latency?

## Done when
- [ ] You have a live Grafana dashboard with TTFT, ITL, throughput, queue depth, KV util.
- [ ] You proposed concrete p95 SLOs grounded in your measurements.
- [ ] You can explain why average latency is the wrong headline metric.

## Common pitfalls
- Averaging hides tail latency — always look at p95/p99, not the mean.
- TTFT and ITL are separate SLOs; a good average can hide a bad streaming experience.

## Resources
- [[vLLM Documentation]]
- [[Grafana Labs & Red Hat (OpenShift AI)]]

## Go deeper
- A production "how we set LLM SLOs" engineering post.
- The Grafana/Red Hat vLLM observability reference dashboard.

## Tasks
- [ ] Study/open [[vLLM Documentation]]
- [ ] Study/open [[Grafana Labs & Red Hat (OpenShift AI)]]
- [ ] **Build:** Add Prometheus + Grafana to your vLLM deployment; build a dashboard with TTFT, ITL, throughput, queue depth, KV utilization.
- [ ] You have a live Grafana dashboard with TTFT, ITL, throughput, queue depth, KV util.
- [ ] You proposed concrete p95 SLOs grounded in your measurements.
- [ ] You can explain why average latency is the wrong headline metric.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
