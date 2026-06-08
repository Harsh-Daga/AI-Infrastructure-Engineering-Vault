---
type: "concept"
area: "[[Inference Infrastructure]]"
difficulty: 3
mastery: 0
prerequisites: ["[[PagedAttention]]", "[[KV Cache]]"]
unlocks: ["[[KV Routing]]"]
tags: ["concept", "area/inference-infrastructure"]
---

# RadixAttention and Prefix Caching

Automatic reuse of KV for shared prefixes (same system prompt, few-shot examples, agent scaffolding) via a radix tree over cached blocks. Workloads with heavy prefix overlap (agents, RAG with a fixed system prompt) win big; workloads with unique prompts don't.

> [!info] Why it matters for an infra engineer
> Whether prefix caching helps is a property of *your* workload. Knowing this decides SGLang-vs-vLLM and how you design system prompts.

## Related

- **Area:** [[Inference Infrastructure]]
- **Prerequisites:** [[PagedAttention]], [[KV Cache]]
- **Unlocks:** [[KV Routing]]
- **Studied in:** [[Week 11 — SGLang & RadixAttention]], [[Week 15 — KV cache management & offloading]]
- **Resources:** [[SGLang Documentation]], [[RadixAttention (SGLang)]], [[sglang]]

## Notes
