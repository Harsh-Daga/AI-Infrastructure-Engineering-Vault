---
type: "phase"
phase: 2
weeks: "9-16"
status: "not-started"
tags: ["phase", "phase/2"]
---

# Phase 2 — LLM Serving, Deep

> Become genuinely good at turning a model + GPUs into a fast, reliable, cost-aware API. This is the skill that pays the bills.

**Weeks:** 9–16  
**Phase deliverable lands in:** [[Week 16 — Multi-GPU single-node serving]]

## Weeks

- [[Week 09 — Serving fundamentals — batching]]
- [[Week 10 — vLLM in depth]]
- [[Week 11 — SGLang & RadixAttention]]
- [[Week 12 — TensorRT-LLM, Triton, and NIM]]
- [[Week 13 — Speculative decoding & latency tricks]]
- [[Week 14 — Serving metrics, SLOs & load testing]]
- [[Week 15 — KV cache management & offloading]]
- [[Week 16 — Multi-GPU single-node serving]]

## Progress (Dataview)
<!-- Requires Dataview. Shows the status of every week in this phase. -->
```dataview
TABLE status, objective
FROM #week
WHERE phase = "Phase 2 — LLM Serving, Deep"
SORT week ASC
```
