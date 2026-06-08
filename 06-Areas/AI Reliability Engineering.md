---
type: "area"
ranked: "yes"
demand: 5
comp: 5
depth: 5
difficulty: 4
longevity: 5
tags: ["area", "area/ai-reliability-engineering"]
---

# AI Reliability Engineering

> SLOs, fault tolerance, cluster health for GPU/training.

## Part 1 ranking (1–5)
| Demand | Comp | Depth | Difficulty | Longevity |
|---|---|---|---|---|
| 5 | 5 | 5 | 4 | 5 |

## Concepts in this area

- [[AI Reliability Engineering]]
- [[Checkpointing and Fault Tolerance]]
- [[Stragglers and SDC]]

## Weeks that cover it

- [[Week 39 — Checkpointing, fault tolerance, elastic training]]
- [[Week 40 — Silent failures, stragglers & reliability]]
- [[Week 43 — AI reliability engineering — SLOs & error budgets]]
- [[Week 44 — Failure injection & chaos for AI]]

## Projects

- [[Level 7 — Production-grade AI platform]]

## Resources

- [[Google SRE Book & Workbook]]
- [[Uber, Netflix & Stripe Engineering]]

## Live view (DataviewJS)
<!-- Requires the Dataview plugin. Lists every note tagged to this area automatically. -->
```dataviewjs
const slug = "area/ai-reliability-engineering";
const pages = dv.pages("#" + slug).sort(p => p.type);
dv.table(["Note", "Type", "Difficulty", "Status/Mastery"],
  pages.map(p => [p.file.link, p.type, p.difficulty ?? "",
    p.status ?? (p.mastery !== undefined ? "mastery " + p.mastery : "")]));
```
