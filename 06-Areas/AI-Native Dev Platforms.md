---
type: "area"
ranked: "yes"
demand: 4
comp: 5
depth: 4
difficulty: 4
longevity: 5
tags: ["area", "area/ai-native-dev-platforms"]
---

# AI-Native Dev Platforms

> Internal platforms purpose-built for AI engineers.

## Part 1 ranking (1–5)
| Demand | Comp | Depth | Difficulty | Longevity |
|---|---|---|---|---|
| 4 | 5 | 4 | 4 | 5 |

## Live view (DataviewJS)
<!-- Requires the Dataview plugin. Lists every note tagged to this area automatically. -->
```dataviewjs
const slug = "area/ai-native-dev-platforms";
const pages = dv.pages("#" + slug).sort(p => p.type);
dv.table(["Note", "Type", "Difficulty", "Status/Mastery"],
  pages.map(p => [p.file.link, p.type, p.difficulty ?? "",
    p.status ?? (p.mastery !== undefined ? "mastery " + p.mastery : "")]));
```
