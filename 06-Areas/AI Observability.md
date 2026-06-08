---
type: "area"
ranked: "yes"
demand: 5
comp: 4
depth: 3
difficulty: 2
longevity: 5
tags: ["area", "area/ai-observability"]
---

# AI Observability

> Traces/metrics/cost/eval for non-deterministic model + agent systems.

## Part 1 ranking (1–5)
| Demand | Comp | Depth | Difficulty | Longevity |
|---|---|---|---|---|
| 5 | 4 | 3 | 2 | 5 |

## Concepts in this area

- [[Eval as Infrastructure]]
- [[OTel GenAI Conventions]]

## Weeks that cover it

- [[Week 22 — AI observability with OTel GenAI]]
- [[Week 23 — Evaluation as infrastructure]]

## Projects

- [[Level 2 — RAG with hybrid search & observability]]
- [[Level 3 — Multi-model routing gateway + cost optimization]]
- [[Level 7 — Production-grade AI platform]]

## Resources

- [[OpenTelemetry GenAI Semantic Conventions]]
- [[Uber, Netflix & Stripe Engineering]]
- [[Grafana Labs & Red Hat (OpenShift AI)]]
- [[langfuse]]
- [[phoenix]]

## Live view (DataviewJS)
<!-- Requires the Dataview plugin. Lists every note tagged to this area automatically. -->
```dataviewjs
const slug = "area/ai-observability";
const pages = dv.pages("#" + slug).sort(p => p.type);
dv.table(["Note", "Type", "Difficulty", "Status/Mastery"],
  pages.map(p => [p.file.link, p.type, p.difficulty ?? "",
    p.status ?? (p.mastery !== undefined ? "mastery " + p.mastery : "")]));
```
