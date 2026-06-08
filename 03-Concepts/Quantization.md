---
type: "concept"
area: "[[AI Cost Optimization]]"
difficulty: 3
mastery: 0
prerequisites: ["[[GPU Memory Hierarchy]]"]
unlocks: ["[[AI Cost Engineering]]"]
tags: ["concept", "area/ai-cost-optimization"]
---

# Quantization

Representing weights/activations in fewer bits (FP16/BF16 → FP8/INT8/INT4) to cut memory and raise throughput. FP8 on Hopper/Blackwell is a big lever. The tradeoff is precision vs quality vs memory — sometimes free lunch, sometimes a quiet quality tax you only catch with evals. The highest-ROI inference lever you'll actually pull.

> [!info] Why it matters for an infra engineer
> Quantization is the single biggest knob on cost-per-token you can turn without re-architecting anything. Know when it's free and when it costs quality.

## Related

- **Area:** [[AI Cost Optimization]]
- **Prerequisites:** [[GPU Memory Hierarchy]]
- **Unlocks:** [[AI Cost Engineering]]
- **Studied in:** [[Week 06 — Precision & quantization]]
- **Resources:** [[Hugging Face Blog]], [[Speculative Decoding]]
- **Projects:** [[Level 1 — Run local LLMs]], [[Level 3 — Multi-model routing gateway + cost optimization]]

## Notes
