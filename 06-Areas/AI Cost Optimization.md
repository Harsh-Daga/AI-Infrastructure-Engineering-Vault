---
type: "area"
ranked: "yes"
demand: 5
comp: 5
depth: 4
difficulty: 3
longevity: 5
tags: ["area", "area/ai-cost-optimization"]
---

# AI Cost Optimization

> Moving the GPU bill: utilization, quant, routing, spot.

## Part 1 ranking (1–5)
| Demand | Comp | Depth | Difficulty | Longevity |
|---|---|---|---|---|
| 5 | 5 | 4 | 3 | 5 |

## Concepts in this area

- [[AI Cost Engineering]]
- [[Distillation]]
- [[Fine-tuning and RLHF]]
- [[Quantization]]

## Weeks that cover it

- [[Week 06 — Precision & quantization]]
- [[Week 08 — Model families & what they cost to run]]
- [[Week 24 — AI cost optimization]]

## Projects

- [[Level 1 — Run local LLMs]]
- [[Level 3 — Multi-model routing gateway + cost optimization]]

## Resources

- [[Character.AI, Cursor & Perplexity Engineering]]
- [[SemiAnalysis]]

## Live view (DataviewJS)
<!-- Requires the Dataview plugin. Lists every note tagged to this area automatically. -->
```dataviewjs
const slug = "area/ai-cost-optimization";
const pages = dv.pages("#" + slug).sort(p => p.type);
dv.table(["Note", "Type", "Difficulty", "Status/Mastery"],
  pages.map(p => [p.file.link, p.type, p.difficulty ?? "",
    p.status ?? (p.mastery !== undefined ? "mastery " + p.mastery : "")]));
```
