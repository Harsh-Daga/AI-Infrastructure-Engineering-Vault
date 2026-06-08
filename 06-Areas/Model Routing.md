---
type: "area"
ranked: "yes"
demand: 4
comp: 4
depth: 3
difficulty: 3
longevity: 4
tags: ["area", "area/model-routing"]
---

# Model Routing

> Quality/cost/latency-aware request routing.

## Part 1 ranking (1–5)
| Demand | Comp | Depth | Difficulty | Longevity |
|---|---|---|---|---|
| 4 | 4 | 3 | 3 | 4 |

## Concepts in this area

- [[Model Routing]]

## Weeks that cover it

- [[Week 21 — Model routing]]

## Projects

- [[Level 3 — Multi-model routing gateway + cost optimization]]

## Resources

- [[litellm]]

## Live view (DataviewJS)
<!-- Requires the Dataview plugin. Lists every note tagged to this area automatically. -->
```dataviewjs
const slug = "area/model-routing";
const pages = dv.pages("#" + slug).sort(p => p.type);
dv.table(["Note", "Type", "Difficulty", "Status/Mastery"],
  pages.map(p => [p.file.link, p.type, p.difficulty ?? "",
    p.status ?? (p.mastery !== undefined ? "mastery " + p.mastery : "")]));
```
