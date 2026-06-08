---
type: "concept"
area: "[[LLM Serving]]"
difficulty: 2
mastery: 0
prerequisites: ["[[Prefill vs Decode]]"]
unlocks: ["[[Inference Autoscaling]]", "[[Model Routing]]", "[[Speculative Decoding]]"]
tags: ["concept", "area/llm-serving"]
---

# TTFT vs ITL

Two separate latency SLOs: **TTFT** (time to first token, dominated by prefill + queueing) and **ITL/TBT** (inter-token latency, dominated by decode bandwidth). Plus goodput and p50/p95/p99. Average latency hides the truth for token streams; you must SLO the two phases independently.

> [!info] Why it matters for an infra engineer
> You can't set a single 'latency' SLO for streaming generation. Separating TTFT and ITL is how you actually measure user-perceived quality.

## Related

- **Area:** [[LLM Serving]]
- **Prerequisites:** [[Prefill vs Decode]]
- **Unlocks:** [[Inference Autoscaling]], [[Model Routing]], [[Speculative Decoding]]
- **Studied in:** [[Week 09 — Serving fundamentals — batching]], [[Week 14 — Serving metrics, SLOs & load testing]]
- **Resources:** [[vLLM Documentation]]
- **Projects:** [[Level 1 — Run local LLMs]]

## Notes
