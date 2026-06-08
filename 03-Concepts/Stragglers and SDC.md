---
type: "concept"
area: "[[AI Reliability Engineering]]"
difficulty: 5
mastery: 0
prerequisites: ["[[Collective Communication (NCCL)]]", "[[Checkpointing and Fault Tolerance]]"]
unlocks: ["[[AI Reliability Engineering]]"]
tags: ["concept", "area/ai-reliability-engineering"]
---

# Stragglers and SDC

The hardest reliability problems: a single **straggler** (slow node) stalls a synchronous all-reduce and thus thousands of GPUs; **silent data corruption** (SDC) produces wrong results with no error. Plus NCCL hangs. Detection needs pre/post-run health checks and continuous monitoring.

> [!info] Why it matters for an infra engineer
> Debugging a NCCL hang or a straggler at 3am is a skill almost no one has and everyone needs. This is the rare, staff-level reliability work.

## Related

- **Area:** [[AI Reliability Engineering]]
- **Prerequisites:** [[Collective Communication (NCCL)]], [[Checkpointing and Fault Tolerance]]
- **Unlocks:** [[AI Reliability Engineering]]
- **Studied in:** [[Week 39 — Checkpointing, fault tolerance, elastic training]], [[Week 40 — Silent failures, stragglers & reliability]]
- **Resources:** [[nccl]], [[Meta Engineering & PyTorch Blog]]
- **Projects:** [[Level 7 — Production-grade AI platform]]

## Notes
