---
type: "area"
ranked: "yes"
demand: 5
comp: 4
depth: 4
difficulty: 3
longevity: 5
tags: ["area", "area/agent-infrastructure"]
---

# Agent Infrastructure

> Durable execution, memory, tools, multi-agent coordination.

## Part 1 ranking (1–5)
| Demand | Comp | Depth | Difficulty | Longevity |
|---|---|---|---|---|
| 5 | 4 | 4 | 3 | 5 |

## Concepts in this area

- [[Durable Execution]]
- [[Multi-Agent and A2A]]

## Weeks that cover it

- [[Week 45 — Agent infrastructure & durable execution]]
- [[Week 48 — Multi-agent infrastructure]]

## Projects

- [[Level 7 — Production-grade AI platform]]

## Resources

- [[MCP Specification & 2026 Roadmap]]
- [[Anthropic Engineering]]
- [[temporal]]
- [[restate]]
- [[Latent Space (newsletter & podcast)]]

## Live view (DataviewJS)
<!-- Requires the Dataview plugin. Lists every note tagged to this area automatically. -->
```dataviewjs
const slug = "area/agent-infrastructure";
const pages = dv.pages("#" + slug).sort(p => p.type);
dv.table(["Note", "Type", "Difficulty", "Status/Mastery"],
  pages.map(p => [p.file.link, p.type, p.difficulty ?? "",
    p.status ?? (p.mastery !== undefined ? "mastery " + p.mastery : "")]));
```
