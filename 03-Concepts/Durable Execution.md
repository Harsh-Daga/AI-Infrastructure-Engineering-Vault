---
type: "concept"
area: "[[Agent Infrastructure]]"
difficulty: 3
mastery: 0
prerequisites: ["[[Queueing and Backpressure]]"]
unlocks: ["[[Multi-Agent and A2A]]"]
tags: ["concept", "area/agent-infrastructure"]
---

# Durable Execution

Engines (Temporal, Restate) that persist workflow state so a multi-step, long-running agent **survives a worker crash and resumes** — with retries, idempotency, and timers. Agents are a workflow-orchestration problem more than a model problem.

> [!info] Why it matters for an infra engineer
> Pick one durable-execution engine and go deep. It's what turns flaky multi-step agents into production systems that recover.

## Related

- **Area:** [[Agent Infrastructure]]
- **Prerequisites:** [[Queueing and Backpressure]]
- **Unlocks:** [[Multi-Agent and A2A]]
- **Studied in:** [[Week 45 — Agent infrastructure & durable execution]]
- **Resources:** [[temporal]], [[restate]]
- **Projects:** [[Level 7 — Production-grade AI platform]]

## Notes
