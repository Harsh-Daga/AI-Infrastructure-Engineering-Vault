---
type: "concept"
area: "[[AI Workload Scheduling]]"
difficulty: 4
mastery: 0
prerequisites: ["[[DRA]]"]
unlocks: []
tags: ["concept", "area/ai-workload-scheduling"]
---

# Gang Scheduling

All-or-nothing placement: a distributed job's pods all start together or none do (plus priority, preemption, quotas, fair share). Without it, a multi-pod training job can deadlock holding partial resources while others wait.

> [!info] Why it matters for an infra engineer
> A distributed training job *requires* gang scheduling. Co-scheduling train/batch/online with fair share is a high-comp, largely-unsolved problem.

## Related

- **Area:** [[AI Workload Scheduling]]
- **Prerequisites:** [[DRA]]
- **Studied in:** [[Week 28 — AI-aware scheduling & gang scheduling]]
- **Resources:** [[KAI-Scheduler]], [[volcano]], [[kueue]], [[CNCF — KubeCon talks]]
- **Projects:** [[Level 5 — GPU scheduling deep-dive]]

## Notes
