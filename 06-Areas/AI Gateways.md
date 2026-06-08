---
type: "area"
ranked: "yes"
demand: 4
comp: 3
depth: 3
difficulty: 2
longevity: 4
tags: ["area", "area/ai-gateways"]
---

# AI Gateways

> The multi-model edge: auth, budgets, routing, guardrails.

## Part 1 ranking (1–5)
| Demand | Comp | Depth | Difficulty | Longevity |
|---|---|---|---|---|
| 4 | 3 | 3 | 2 | 4 |

## Concepts in this area

- [[AI Gateway]]

## Weeks that cover it

- [[Week 20 — AI gateways — the multi-model edge]]

## Projects

- [[Level 3 — Multi-model routing gateway + cost optimization]]

## Resources

- [[Cloudflare Blog]]
- [[litellm]]
- [[ai-gateway]]
- [[Portkey-gateway]]

## Live view (DataviewJS)
<!-- Requires the Dataview plugin. Lists every note tagged to this area automatically. -->
```dataviewjs
const slug = "area/ai-gateways";
const pages = dv.pages("#" + slug).sort(p => p.type);
dv.table(["Note", "Type", "Difficulty", "Status/Mastery"],
  pages.map(p => [p.file.link, p.type, p.difficulty ?? "",
    p.status ?? (p.mastery !== undefined ? "mastery " + p.mastery : "")]));
```
