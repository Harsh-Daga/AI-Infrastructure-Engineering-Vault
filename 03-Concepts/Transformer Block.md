---
type: "concept"
area: "[[LLM Serving]]"
difficulty: 3
mastery: 0
prerequisites: ["[[Attention]]"]
unlocks: ["[[Distillation]]", "[[Fine-tuning and RLHF]]", "[[KV Cache]]", "[[Mixture of Experts]]", "[[Prefill vs Decode]]", "[[Reasoning Models]]"]
tags: ["concept", "area/llm-serving"]
---

# Transformer Block

A transformer layer = attention + feed-forward (MLP) + norms + residuals, stacked N times. For infra, what matters is what each layer *holds in memory*: weights (fixed), activations (scale with batch × sequence during prefill), and per-layer KV (grows with context). Total VRAM = weights + KV cache + activation/working memory.

> [!info] Why it matters for an infra engineer
> Knowing what each layer stores lets you predict VRAM and find the OOM cliff before you hit it.

## Related

- **Area:** [[LLM Serving]]
- **Prerequisites:** [[Attention]]
- **Unlocks:** [[Distillation]], [[Fine-tuning and RLHF]], [[KV Cache]], [[Mixture of Experts]], [[Prefill vs Decode]], [[Reasoning Models]]
- **Studied in:** [[Week 03 — Attention & the transformer, infra lens]]
- **Resources:** [[Jay Alammar — The Illustrated Transformer]], [[Attention Is All You Need]]

## Notes
