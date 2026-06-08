---
type: "concept"
area: "[[Inference Infrastructure]]"
difficulty: 3
mastery: 0
prerequisites: []
unlocks: ["[[Durable Execution]]", "[[Inference Autoscaling]]"]
tags: ["concept", "area/inference-infrastructure"]
---

# Queueing and Backpressure

Inference is a queueing problem: request queues, admission control, backpressure under load, and load-shedding. Data/synthetic pipelines are streaming problems. Little's Law and tail behavior under saturation are the tools.

> [!info] Why it matters for an infra engineer
> Under load, the queue *is* your latency. Admission control and backpressure are what keep TTFT from cliffing when traffic spikes.

## Related

- **Area:** [[Inference Infrastructure]]
- **Unlocks:** [[Durable Execution]], [[Inference Autoscaling]]
- **Studied in:** [[Week 09 — Serving fundamentals — batching]], [[Week 36 — Distributed systems for AI — coordination]]
- **Resources:** [[Designing Data-Intensive Applications]]
- **Projects:** [[Level 3 — Multi-model routing gateway + cost optimization]]

## Notes
