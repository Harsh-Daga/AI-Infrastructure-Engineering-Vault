---
type: "concept"
area: "[[Inference Infrastructure]]"
difficulty: 2
mastery: 0
prerequisites: ["[[Prefill vs Decode]]", "[[Transformer Block]]"]
unlocks: []
tags: ["concept", "area/inference-infrastructure"]
---

# Reasoning Models

Reasoning models spend many tokens "thinking" before answering — i.e. **long decode**. That shifts the infra bill toward decode (memory-bandwidth-bound, KV-cache-heavy) and changes capacity planning: more decode GPUs, bigger KV budgets, latency dominated by inter-token time.

> [!info] Why it matters for an infra engineer
> A reasoning model can flip your prefill/decode capacity ratio overnight. Know how model choice rewrites your serving plan.

## Related

- **Area:** [[Inference Infrastructure]]
- **Prerequisites:** [[Prefill vs Decode]], [[Transformer Block]]
- **Studied in:** [[Week 08 — Model families & what they cost to run]]
- **Resources:** [[Llama, DeepSeek & Qwen Technical Reports]]

## Notes
