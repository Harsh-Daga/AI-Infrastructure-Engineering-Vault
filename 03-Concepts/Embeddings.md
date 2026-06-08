---
type: "concept"
area: "[[Vector Databases]]"
difficulty: 1
mastery: 0
prerequisites: ["[[Tokenization]]"]
unlocks: ["[[Attention]]", "[[RAG]]", "[[Vector Search (HNSW and IVF)]]"]
tags: ["concept", "area/vector-databases"]
---

# Embeddings

An embedding maps a token (or a whole chunk of text) into a dense vector in high-dimensional space, where geometric closeness approximates semantic similarity. Token embeddings feed the transformer; document embeddings are the unit of **retrieval**. Their dimensionality and dtype determine vector-store memory and ANN-index cost.

> [!info] Why it matters for an infra engineer
> Embeddings are the storage unit of every RAG and memory system. Their size drives vector-DB RAM and recall/latency tradeoffs.

## Related

- **Area:** [[Vector Databases]]
- **Prerequisites:** [[Tokenization]]
- **Unlocks:** [[Attention]], [[RAG]], [[Vector Search (HNSW and IVF)]]
- **Studied in:** [[Week 02 — Tokenization, embeddings, context windows]], [[Week 17 — Embeddings, vector search & ANN indexes]]
- **Resources:** [[Hugging Face NLP Course]]

## Notes
