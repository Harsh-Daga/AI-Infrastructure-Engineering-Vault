---
type: "phase"
phase: 4
weeks: "25-32"
status: "not-started"
tags: ["phase", "phase/4"]
---

# Phase 4 — GPU Orchestration & the AI Platform on Kubernetes

> Your superpower phase. You already know Kubernetes; now learn the GPU-native control plane that almost no one else has hands-on.

**Weeks:** 25–32  
**Phase deliverable lands in:** [[Week 32 — GPU node observability with eBPF]]

## Projects in this phase

- [[Level 4 — AI platform on Kubernetes]]
- [[Level 5 — GPU scheduling deep-dive]]

## Weeks

- [[Week 25 — GPUs on Kubernetes — the device-plugin era]]
- [[Week 26 — Dynamic Resource Allocation (DRA)]]
- [[Week 27 — GPU sharing — MIG, MPS, time-slicing]]
- [[Week 28 — AI-aware scheduling & gang scheduling]]
- [[Week 29 — Inference on Kubernetes — KServe & Ray]]
- [[Week 30 — Disaggregated serving — Dynamo & llm-d]]
- [[Week 31 — The internal AI platform (paved road)]]
- [[Week 32 — GPU node observability with eBPF]]

## Progress (Dataview)
<!-- Requires Dataview. Shows the status of every week in this phase. -->
```dataview
TABLE status, objective
FROM #week
WHERE phase = "Phase 4 — GPU Orchestration & the AI Platform on Kubernetes"
SORT week ASC
```
