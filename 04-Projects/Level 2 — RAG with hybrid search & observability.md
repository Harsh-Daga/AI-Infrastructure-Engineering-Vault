---
type: "project"
level: 2
status: "not-started"
phase: "[[Phase 3 — Inference Infrastructure]]"
skills: ["[[RAG]]", "[[Vector Search (HNSW and IVF)]]", "[[Hybrid Search]]", "[[Embeddings]]", "[[OTel GenAI Conventions]]", "[[Eval as Infrastructure]]"]
repos: ["[[qdrant]]", "[[pgvector]]", "[[langfuse]]", "[[phoenix]]"]
success-criteria: "A measured retrieval-quality metric, a full end-to-end trace per request, and a documented \"why naive RAG failed and what fixed it.\""
tags: ["project", "level/2"]
---

# Level 2 — RAG with hybrid search & observability

**Phase:** [[Phase 3 — Inference Infrastructure]]  
**Weeks:** [[Week 17 — Embeddings, vector search & ANN indexes]], [[Week 18 — RAG as a system]], [[Week 19 — Hybrid search & retrieval quality]], [[Week 22 — AI observability with OTel GenAI]]

## Architecture
ingest → embed → vector store (pgvector/Qdrant) → hybrid retrieval (BM25 + dense) → rerank → LLM, fully traced with OTel.

## Components
embedding service, vector index, reranker, retrieval eval set, OTel + Langfuse/Phoenix.

## Why it matters
RAG is everywhere; doing it with retrieval eval and tracing (not naive top-k) is what separates a platform engineer from a tutorial follower.

## Skills learned
ANN index ops, hybrid search, retrieval evaluation, GenAI tracing, cost/token attribution.

## Skills (concept links)

- [[RAG]]
- [[Vector Search (HNSW and IVF)]]
- [[Hybrid Search]]
- [[Embeddings]]
- [[OTel GenAI Conventions]]
- [[Eval as Infrastructure]]

## Success criteria
> A measured retrieval-quality metric, a full end-to-end trace per request, and a documented "why naive RAG failed and what fixed it."

## Repos to study
[[qdrant]], [[pgvector]], [[langfuse]], [[phoenix]]

## Build log
_Log progress here as you build._


## Tasks
- [ ] Scaffold the repo with a real README and architecture doc
- [ ] Implement the core architecture above
- [ ] Produce the benchmark / cost model that proves the success criteria
- [ ] Write the "what I learned" section and publish to the learning log
