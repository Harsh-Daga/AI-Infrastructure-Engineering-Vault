---
type: "concept"
area: "[[Vector Databases]]"
difficulty: 2
mastery: 0
prerequisites: ["[[Embeddings]]"]
unlocks: ["[[Agent Memory]]", "[[Hybrid Search]]", "[[RAG]]"]
tags: ["concept", "area/vector-databases"]
---

# Vector Search (HNSW and IVF)

Approximate nearest-neighbor indexes (HNSW graph, IVF clusters, PQ compression) that trade recall for latency/memory. A vector DB is "just" an ANN index + a serving layer; the real operational difficulty is recall tuning, memory, and updates at scale.

> [!info] Why it matters for an infra engineer
> It's the easiest area to learn (a weekend) and therefore the least defensible — but you must operate one correctly for any RAG/memory system.

## Related

- **Area:** [[Vector Databases]]
- **Prerequisites:** [[Embeddings]]
- **Unlocks:** [[Agent Memory]], [[Hybrid Search]], [[RAG]]
- **Studied in:** [[Week 17 — Embeddings, vector search & ANN indexes]]
- **Resources:** [[qdrant]], [[pgvector]], [[faiss]]
- **Projects:** [[Level 2 — RAG with hybrid search & observability]]

## Notes
