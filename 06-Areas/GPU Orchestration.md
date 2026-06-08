---
type: "area"
ranked: "yes"
demand: 5
comp: 5
depth: 4
difficulty: 4
longevity: 5
tags: ["area", "area/gpu-orchestration"]
---

# GPU Orchestration

> Scheduling/sharing GPUs (DRA, KAI, MIG, gang scheduling).

## Part 1 ranking (1–5)
| Demand | Comp | Depth | Difficulty | Longevity |
|---|---|---|---|---|
| 5 | 5 | 4 | 4 | 5 |

## Concepts in this area

- [[DRA]]
- [[GPU Sharing (MIG and MPS)]]

## Weeks that cover it

- [[Week 26 — Dynamic Resource Allocation (DRA)]]
- [[Week 27 — GPU sharing — MIG, MPS, time-slicing]]

## Projects

- [[Level 4 — AI platform on Kubernetes]]
- [[Level 5 — GPU scheduling deep-dive]]

## Resources

- [[Kubernetes DRA Documentation]]
- [[AWS — AI on EKS Guide]]
- [[NVIDIA GPU Operator Documentation]]
- [[Grafana Labs & Red Hat (OpenShift AI)]]
- [[llm-d]]
- [[k8s-dra-driver]]
- [[gpu-operator]]
- [[KAI-Scheduler]]
- [[CNCF — KubeCon talks]]

## Live view (DataviewJS)
<!-- Requires the Dataview plugin. Lists every note tagged to this area automatically. -->
```dataviewjs
const slug = "area/gpu-orchestration";
const pages = dv.pages("#" + slug).sort(p => p.type);
dv.table(["Note", "Type", "Difficulty", "Status/Mastery"],
  pages.map(p => [p.file.link, p.type, p.difficulty ?? "",
    p.status ?? (p.mastery !== undefined ? "mastery " + p.mastery : "")]));
```
