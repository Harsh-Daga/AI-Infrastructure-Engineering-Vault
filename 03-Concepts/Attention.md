---
type: "concept"
area: "[[LLM Serving]]"
difficulty: 3
mastery: 0
prerequisites: ["[[Embeddings]]"]
unlocks: ["[[Context Parallelism]]", "[[FlashAttention]]", "[[KV Cache]]", "[[Transformer Block]]"]
tags: ["concept", "area/llm-serving"]
---

# Attention

Self-attention lets every token attend to every other token, which is why a transformer is **O(n²)** in sequence length and why long contexts are expensive. The key insight for infra: attention is the reason the **KV cache** exists — past keys/values are recomputed-or-cached to avoid quadratic recompute every decode step. You need the *shapes* and the *memory cost*, not the gradient math.

> [!info] Why it matters for an infra engineer
> Attention's quadratic cost and its key/value tensors are the root cause of nearly every inference memory problem you will debug.

## Related

- **Area:** [[LLM Serving]]
- **Prerequisites:** [[Embeddings]]
- **Unlocks:** [[Context Parallelism]], [[FlashAttention]], [[KV Cache]], [[Transformer Block]]
- **Studied in:** [[Week 03 — Attention & the transformer, infra lens]]
- **Resources:** [[Jay Alammar — The Illustrated Transformer]], [[Attention Is All You Need]], [[3Blue1Brown — Neural Networks series]]

## Notes
