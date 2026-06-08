---
type: "concept"
area: "[[Inference Infrastructure]]"
difficulty: 3
mastery: 0
prerequisites: ["[[Consistency Models]]"]
unlocks: []
tags: ["concept", "area/inference-infrastructure"]
---

# Raft

The consensus protocol behind etcd and most control planes. You'll **operate** Raft-backed systems (Kubernetes, schedulers, discovery) far more than implement them; understand leader election, log replication, and what a quorum loss means.

> [!info] Why it matters for an infra engineer
> Your control planes (K8s/etcd, schedulers) are Raft-backed. Knowing its failure behavior is core to operating them under partition.

## Related

- **Area:** [[Inference Infrastructure]]
- **Prerequisites:** [[Consistency Models]]
- **Studied in:** [[Week 36 — Distributed systems for AI — coordination]]
- **Resources:** [[Designing Data-Intensive Applications]], [[MIT 6.824 Distributed Systems]]

## Notes
