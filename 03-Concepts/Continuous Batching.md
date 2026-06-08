---
type: "concept"
area: "[[LLM Serving]]"
difficulty: 3
mastery: 0
prerequisites: ["[[Prefill vs Decode]]", "[[KV Cache]]"]
unlocks: []
tags: ["concept", "area/llm-serving"]
---

# Continuous Batching

Instead of fixed batches, the scheduler admits and retires requests token-by-token, keeping the GPU saturated as sequences of different lengths come and go. It's the core reason modern engines (vLLM/SGLang) beat naive servers on throughput without wrecking latency.

> [!info] Why it matters for an infra engineer
> It's the default that makes GPU serving economical. Understanding it explains why TTFT explodes on naive setups and how admission control fixes it.

## Related

- **Area:** [[LLM Serving]]
- **Prerequisites:** [[Prefill vs Decode]], [[KV Cache]]
- **Studied in:** [[Week 09 — Serving fundamentals — batching]]
- **Resources:** [[Anyscale — Continuous Batching Blog]], [[vLLM Documentation]]
- **Projects:** [[Level 1 — Run local LLMs]]

## Notes
