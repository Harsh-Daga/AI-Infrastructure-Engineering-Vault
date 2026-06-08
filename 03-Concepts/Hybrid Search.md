---
type: "concept"
area: "[[Retrieval Systems]]"
difficulty: 3
mastery: 0
prerequisites: ["[[Vector Search (HNSW and IVF)]]"]
unlocks: ["[[RAG]]"]
tags: ["concept", "area/retrieval-systems"]
---

# Hybrid Search

Fusing lexical (BM25) and dense retrieval, then reranking, to beat either alone — plus freshness. Retrieval quality needs its own offline eval set and metric, separate from answer quality.

> [!info] Why it matters for an infra engineer
> Naive top-k is a tutorial; hybrid search + reranking + retrieval eval is what separates a platform engineer from a tutorial follower.

## Related

- **Area:** [[Retrieval Systems]]
- **Prerequisites:** [[Vector Search (HNSW and IVF)]]
- **Unlocks:** [[RAG]]
- **Studied in:** [[Week 19 — Hybrid search & retrieval quality]]
- **Resources:** [[qdrant]], [[Character.AI, Cursor & Perplexity Engineering]]
- **Projects:** [[Level 2 — RAG with hybrid search & observability]]

## Notes
