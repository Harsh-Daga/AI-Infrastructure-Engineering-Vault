---
type: "area"
ranked: "yes"
demand: 4
comp: 4
depth: 3
difficulty: 3
longevity: 4
tags: ["area", "area/multi-model-systems"]
---

# Multi-Model Systems

> Operating fleets of heterogeneous models.

## Part 1 ranking (1–5)
| Demand | Comp | Depth | Difficulty | Longevity |
|---|---|---|---|---|
| 4 | 4 | 3 | 3 | 4 |

## Live view (DataviewJS)
<!-- Requires the Dataview plugin. Lists every note tagged to this area automatically. -->
```dataviewjs
const slug = "area/multi-model-systems";
const pages = dv.pages("#" + slug).sort(p => p.type);
dv.table(["Note", "Type", "Difficulty", "Status/Mastery"],
  pages.map(p => [p.file.link, p.type, p.difficulty ?? "",
    p.status ?? (p.mastery !== undefined ? "mastery " + p.mastery : "")]));
```
