---
type: "concept"
area: "[[AI Cost Optimization]]"
difficulty: 2
mastery: 0
prerequisites: ["[[Transformer Block]]"]
unlocks: []
tags: ["concept", "area/ai-cost-optimization"]
---

# Distillation

Training a smaller "student" model to mimic a larger "teacher", yielding a cheaper model at some quality cost. As infra, you don't implement it — you know it produces the small models you route cheap traffic to.

> [!info] Why it matters for an infra engineer
> Distilled small models are the cheap tier in a routing cascade. Know what they are and where they fit the cost story.

## Related

- **Area:** [[AI Cost Optimization]]
- **Prerequisites:** [[Transformer Block]]
- **Studied in:** [[Week 08 — Model families & what they cost to run]]
- **Resources:** [[Hugging Face Blog]]

## Notes
