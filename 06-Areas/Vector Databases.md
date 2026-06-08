---
type: "area"
ranked: "yes"
demand: 3
comp: 3
depth: 3
difficulty: 2
longevity: 3
tags: ["area", "area/vector-databases"]
---

# Vector Databases

> ANN indexes (HNSW/IVF) as a storage/serving system.

## Part 1 ranking (1–5)
| Demand | Comp | Depth | Difficulty | Longevity |
|---|---|---|---|---|
| 3 | 3 | 3 | 2 | 3 |

## Concepts in this area

- [[Embeddings]]
- [[Vector Search (HNSW and IVF)]]

## Weeks that cover it

- [[Week 02 — Tokenization, embeddings, context windows]]
- [[Week 17 — Embeddings, vector search & ANN indexes]]

## Projects

- [[Level 2 — RAG with hybrid search & observability]]

## Resources

- [[qdrant]]
- [[pgvector]]
- [[faiss]]

## Live view (DataviewJS)
<!-- Requires the Dataview plugin. Lists every note tagged to this area automatically. -->
```dataviewjs
const slug = "area/vector-databases";
const pages = dv.pages("#" + slug).sort(p => p.type);
dv.table(["Note", "Type", "Difficulty", "Status/Mastery"],
  pages.map(p => [p.file.link, p.type, p.difficulty ?? "",
    p.status ?? (p.mastery !== undefined ? "mastery " + p.mastery : "")]));
```
