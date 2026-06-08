---
type: "concept"
area: "[[LLM Serving]]"
difficulty: 4
mastery: 0
prerequisites: ["[[Attention]]", "[[GPU Memory Hierarchy]]"]
unlocks: []
tags: ["concept", "area/llm-serving"]
---

# FlashAttention

An IO-aware attention implementation that tiles the computation to keep data in fast SRAM and avoid materializing the giant N×N attention matrix in HBM. It makes attention dramatically faster not by changing the math but by **moving less memory** — the clearest proof that memory movement, not FLOPs, dominates.

> [!info] Why it matters for an infra engineer
> It's the canonical example of the memory-movement-dominates principle, and it's on by default in every serving engine you'll operate.

## Related

- **Area:** [[LLM Serving]]
- **Prerequisites:** [[Attention]], [[GPU Memory Hierarchy]]
- **Studied in:** [[Week 07 — Where the GPU time goes — profiling]]
- **Resources:** [[FlashAttention (1 & 2)]], [[Horace He — Making Deep Learning Go Brrrr]]

## Notes
