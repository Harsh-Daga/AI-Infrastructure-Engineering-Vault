---
type: "area"
ranked: "yes"
demand: 4
comp: 3
depth: 3
difficulty: 3
longevity: 4
tags: ["area", "area/retrieval-systems"]
---

# Retrieval Systems

> Hybrid search, ranking, freshness, retrieval pipelines.

## Part 1 ranking (1–5)
| Demand | Comp | Depth | Difficulty | Longevity |
|---|---|---|---|---|
| 4 | 3 | 3 | 3 | 4 |

## Concepts in this area

- [[Hybrid Search]]
- [[RAG]]

## Weeks that cover it

- [[Week 18 — RAG as a system]]
- [[Week 19 — Hybrid search & retrieval quality]]

## Projects

- [[Level 2 — RAG with hybrid search & observability]]

## Live view (DataviewJS)
<!-- Requires the Dataview plugin. Lists every note tagged to this area automatically. -->
```dataviewjs
const slug = "area/retrieval-systems";
const pages = dv.pages("#" + slug).sort(p => p.type);
dv.table(["Note", "Type", "Difficulty", "Status/Mastery"],
  pages.map(p => [p.file.link, p.type, p.difficulty ?? "",
    p.status ?? (p.mastery !== undefined ? "mastery " + p.mastery : "")]));
```
