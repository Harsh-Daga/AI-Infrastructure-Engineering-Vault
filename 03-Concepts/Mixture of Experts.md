---
type: "concept"
area: "[[Distributed Training]]"
difficulty: 4
mastery: 0
prerequisites: ["[[Transformer Block]]"]
unlocks: ["[[Expert Parallelism]]"]
tags: ["concept", "area/distributed-training"]
---

# Mixture of Experts

MoE replaces a dense FFN with many "expert" FFNs, routing each token to a few. It gives large parameter counts at lower per-token compute — but changes **memory and communication patterns**: experts are sharded (expert parallelism) and routing needs all-to-all comms. Relevant to both serving memory and network design.

> [!info] Why it matters for an infra engineer
> MoE turns a compute problem into a networking problem (all-to-all). It reshapes both your serving memory and your fabric planning.

## Related

- **Area:** [[Distributed Training]]
- **Prerequisites:** [[Transformer Block]]
- **Unlocks:** [[Expert Parallelism]]
- **Studied in:** [[Week 08 — Model families & what they cost to run]]
- **Resources:** [[Switch Transformer & GShard (MoE)]]

## Notes
