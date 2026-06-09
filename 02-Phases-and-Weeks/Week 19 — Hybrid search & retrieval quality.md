---
type: "week"
week: 19
phase: "Phase 3 — Inference Infrastructure"
status: "not-started"
start: 
end: 
objective: "Hybrid search & retrieval quality: BM25 + dense fusion, reranking, freshness, eval."
concepts: ["[[Hybrid Search]]", "[[RAG]]"]
project: ["[[Level 2 — RAG with hybrid search & observability]]"]
deliverable: 
tags: ["week", "phase/3"]
---

# Week 19 — Hybrid search & retrieval quality

**Phase:** [[Phase 3 — Inference Infrastructure]]  
**Objective:** Hybrid search & retrieval quality: BM25 + dense fusion, reranking, freshness, eval.  
**Concepts:** [[Hybrid Search]], [[RAG]]
**Project:** [[Level 2 — RAG with hybrid search & observability]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
Hybrid-search docs (Qdrant/Weaviate/Elasticsearch); reranking model overview.

## Read (15m)
Perplexity/retrieval-at-scale engineering writeups (freshness + ranking + cost).

## Build (20m)
Add BM25 + reranking to your RAG; build a small retrieval eval set and measure improvement.

## Step-by-step
1. Add BM25/keyword search alongside your dense retriever.
2. Fuse results (e.g. Reciprocal Rank Fusion) and add a cross-encoder reranker on top.
3. Build a small labeled retrieval eval set (query → relevant doc ids).
4. Measure retrieval quality (recall@k, MRR/nDCG) for dense vs hybrid vs hybrid+rerank.
5. Correlate the offline retrieval metric with end-to-end answer quality.

## Reflect (5m)
> What's your offline metric for retrieval quality, and how does it correlate with answer quality?

## Done when
- [ ] You measured dense vs hybrid vs hybrid+rerank on a labeled set.
- [ ] You have an offline retrieval metric you trust.
- [ ] You can show how that metric correlates with answer quality.

## Common pitfalls
- Reranking adds latency and cost — measure whether the quality gain justifies it.
- A tiny eval set gives noisy metrics; get enough labeled queries to be meaningful.

## Resources
- [[qdrant]]
- [[Character.AI, Cursor & Perplexity Engineering]]

## Go deeper
- Hybrid-search docs (Qdrant/Weaviate/Elasticsearch).
- A retrieval-at-scale writeup (freshness + ranking + cost).

## Tasks
- [ ] Study/open [[qdrant]]
- [ ] Study/open [[Character.AI, Cursor & Perplexity Engineering]]
- [ ] **Build:** Add BM25 + reranking to your RAG; build a small retrieval eval set and measure improvement.
- [ ] You measured dense vs hybrid vs hybrid+rerank on a labeled set.
- [ ] You have an offline retrieval metric you trust.
- [ ] You can show how that metric correlates with answer quality.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
