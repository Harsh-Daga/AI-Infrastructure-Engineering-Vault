---
type: "concept"
area: "[[Inference Infrastructure]]"
difficulty: 2
mastery: 0
prerequisites: []
unlocks: ["[[Consistency Models]]"]
tags: ["concept", "area/inference-infrastructure"]
---

# CAP

Consistency, Availability, Partition-tolerance: under a network partition you trade C against A. The lens for distributed KV stores, vector DBs, checkpoint stores, and discovery services.

> [!info] Why it matters for an infra engineer
> Every distributed store you'll operate (KV, checkpoints, discovery) sits somewhere on the CAP tradeoff. Name where, on purpose.

## Related

- **Area:** [[Inference Infrastructure]]
- **Unlocks:** [[Consistency Models]]
- **Studied in:** [[Week 36 — Distributed systems for AI — coordination]]
- **Resources:** [[Designing Data-Intensive Applications]], [[MIT 6.824 Distributed Systems]]

## Notes
