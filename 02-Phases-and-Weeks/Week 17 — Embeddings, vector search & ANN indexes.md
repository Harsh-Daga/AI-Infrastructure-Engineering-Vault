---
type: "week"
week: 17
phase: "Phase 3 — Inference Infrastructure"
status: "not-started"
start: 
end: 
objective: "Embeddings, vector search & ANN indexes: HNSW vs IVF as a storage system, not magic."
concepts: ["[[Vector Search (HNSW and IVF)]]", "[[Embeddings]]"]
project: ["[[Level 2 — RAG with hybrid search & observability]]"]
deliverable: 
tags: ["week", "phase/3"]
---

# Week 17 — Embeddings, vector search & ANN indexes

**Phase:** [[Phase 3 — Inference Infrastructure]]  
**Objective:** Embeddings, vector search & ANN indexes: HNSW vs IVF as a storage system, not magic.  
**Concepts:** [[Vector Search (HNSW and IVF)]], [[Embeddings]]
**Project:** [[Level 2 — RAG with hybrid search & observability]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
A solid HNSW explainer; pgvector and Qdrant/Milvus docs intros.

1. Read a solid HNSW explainer (greedy graph navigation, layers).
2. Skim the pgvector and Qdrant/Milvus intro docs.
3. Write the recall-vs-latency knobs for HNSW (m, ef) and IVF (nlist, nprobe).

## Read (15m)
A vector-DB benchmark / "which index when" post.

1. Read a vector-DB "which index when" benchmark.
2. Note the build-time / memory / recall tradeoffs per index.
3. Write which index you'd pick for your corpus size.

## Build (20m)
Stand up pgvector (or Qdrant); index a corpus; measure recall vs latency as you change index params.

## Step-by-step
1. Stand up pgvector (Postgres) or Qdrant via Docker.
2. Embed a real corpus (your docs/notes) and bulk-insert the vectors.
3. Build an HNSW index; query top-k and record recall@k and p95 latency.
4. Sweep index params (HNSW `m`/`ef_construction`/`ef_search`, or IVF `nlist`/`nprobe`) and chart recall vs latency.
5. Compare HNSW vs IVF on the same data for build time, memory, recall, and latency.

## Reflect (5m)
> Why is a vector DB "just" an index + a serving layer, and where's the real operational difficulty?

## Done when
- [ ] You have a recall-vs-latency curve as you change index params.
- [ ] You compared HNSW and IVF tradeoffs on your data.
- [ ] You can explain where the real operational difficulty in a vector DB lives.

## Common pitfalls
- Recall is meaningless without a ground-truth (exact-search) baseline — compute it.
- Bigger `ef_search`/`nprobe` improves recall but costs latency; there's no free accuracy.

## Resources
- [[qdrant]]
- [[pgvector]]
- [[faiss]]

## Go deeper
- A solid HNSW explainer (graph navigation intuition).
- A vector-DB "which index when" benchmark post.

## Tasks
- [ ] Study/open [[qdrant]]
- [ ] Study/open [[pgvector]]
- [ ] Study/open [[faiss]]
- [ ] **Build:** Stand up pgvector (or Qdrant); index a corpus; measure recall vs latency as you change index params.
- [ ] You have a recall-vs-latency curve as you change index params.
- [ ] You compared HNSW and IVF tradeoffs on your data.
- [ ] You can explain where the real operational difficulty in a vector DB lives.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
