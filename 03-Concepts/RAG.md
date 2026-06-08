---
type: "concept"
area: "[[Retrieval Systems]]"
difficulty: 3
mastery: 0
prerequisites: ["[[Hybrid Search]]", "[[Vector Search (HNSW and IVF)]]", "[[Embeddings]]"]
unlocks: ["[[Agent Memory]]"]
tags: ["concept", "area/retrieval-systems"]
---

# RAG

Retrieval-Augmented Generation as a *system*: ingest → chunk → embed → retrieve → rerank → assemble context → generate. Naive RAG fails on stale/irrelevant retrieval and lost-in-the-middle; the fix is retrieval eval, reranking, and context engineering — not magic.

> [!info] Why it matters for an infra engineer
> RAG is everywhere; doing it with retrieval eval and tracing (not naive top-k) is the defensible version. Know which stage causes bad answers.

## Related

- **Area:** [[Retrieval Systems]]
- **Prerequisites:** [[Hybrid Search]], [[Vector Search (HNSW and IVF)]], [[Embeddings]]
- **Unlocks:** [[Agent Memory]]
- **Studied in:** [[Week 18 — RAG as a system]], [[Week 19 — Hybrid search & retrieval quality]]
- **Resources:** [[Character.AI, Cursor & Perplexity Engineering]]
- **Projects:** [[Level 2 — RAG with hybrid search & observability]]

## Notes
