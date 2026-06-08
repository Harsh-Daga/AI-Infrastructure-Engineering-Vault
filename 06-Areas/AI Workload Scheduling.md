---
type: "area"
ranked: "yes"
demand: 4
comp: 5
depth: 5
difficulty: 4
longevity: 5
tags: ["area", "area/ai-workload-scheduling"]
---

# AI Workload Scheduling

> Co-scheduling train/batch/online; fair-share economics.

## Part 1 ranking (1–5)
| Demand | Comp | Depth | Difficulty | Longevity |
|---|---|---|---|---|
| 4 | 5 | 5 | 4 | 5 |

## Concepts in this area

- [[Gang Scheduling]]

## Weeks that cover it

- [[Week 28 — AI-aware scheduling & gang scheduling]]

## Projects

- [[Level 5 — GPU scheduling deep-dive]]

## Resources

- [[Kubernetes DRA Documentation]]
- [[k8s-dra-driver]]
- [[KAI-Scheduler]]
- [[volcano]]
- [[kueue]]
- [[CNCF — KubeCon talks]]

## Live view (DataviewJS)
<!-- Requires the Dataview plugin. Lists every note tagged to this area automatically. -->
```dataviewjs
const slug = "area/ai-workload-scheduling";
const pages = dv.pages("#" + slug).sort(p => p.type);
dv.table(["Note", "Type", "Difficulty", "Status/Mastery"],
  pages.map(p => [p.file.link, p.type, p.difficulty ?? "",
    p.status ?? (p.mastery !== undefined ? "mastery " + p.mastery : "")]));
```
