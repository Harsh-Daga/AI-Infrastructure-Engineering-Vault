---
type: "concept"
area: "[[Inference Infrastructure]]"
difficulty: 2
mastery: 0
prerequisites: ["[[KV Cache]]", "[[Transformer Block]]"]
unlocks: ["[[Continuous Batching]]", "[[Disaggregated Serving]]", "[[Reasoning Models]]", "[[Speculative Decoding]]", "[[TTFT vs ITL]]"]
tags: ["concept", "area/inference-infrastructure"]
---

# Prefill vs Decode

Generation has two phases with **opposite resource profiles**. Prefill processes the whole prompt in one compute-bound pass (big parallel matmuls, fills the KV cache). Decode emits one token at a time, memory-bandwidth-bound, reading the entire model + KV per step. Co-locating them wastes hardware; separating them (disaggregation) lets you scale and tune each independently.

> [!info] Why it matters for an infra engineer
> This split is the mental model behind disaggregated serving, separate TTFT/ITL SLOs, and why you autoscale two pools differently.

## Related

- **Area:** [[Inference Infrastructure]]
- **Prerequisites:** [[KV Cache]], [[Transformer Block]]
- **Unlocks:** [[Continuous Batching]], [[Disaggregated Serving]], [[Reasoning Models]], [[Speculative Decoding]], [[TTFT vs ITL]]
- **Studied in:** [[Week 01 — How an LLM actually runs]], [[Week 08 — Model families & what they cost to run]]
- **Resources:** [[DistServe & Splitwise]]
- **Projects:** [[Level 1 — Run local LLMs]]

## Notes
