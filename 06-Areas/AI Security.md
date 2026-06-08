---
type: "area"
ranked: "yes"
demand: 4
comp: 4
depth: 4
difficulty: 3
longevity: 5
tags: ["area", "area/ai-security"]
---

# AI Security

> Prompt injection, supply chain, model/data exfil, MCP risk.

## Part 1 ranking (1–5)
| Demand | Comp | Depth | Difficulty | Longevity |
|---|---|---|---|---|
| 4 | 4 | 4 | 3 | 5 |

## Resources

- [[OWASP LLM Top 10]]
- [[Import AI]]

## Live view (DataviewJS)
<!-- Requires the Dataview plugin. Lists every note tagged to this area automatically. -->
```dataviewjs
const slug = "area/ai-security";
const pages = dv.pages("#" + slug).sort(p => p.type);
dv.table(["Note", "Type", "Difficulty", "Status/Mastery"],
  pages.map(p => [p.file.link, p.type, p.difficulty ?? "",
    p.status ?? (p.mastery !== undefined ? "mastery " + p.mastery : "")]));
```
