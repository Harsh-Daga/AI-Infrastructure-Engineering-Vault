---
type: "concept"
area: "[[Memory Systems]]"
difficulty: 3
mastery: 0
prerequisites: ["[[KV Cache]]", "[[RAG]]", "[[Vector Search (HNSW and IVF)]]"]
unlocks: ["[[Multi-Agent and A2A]]"]
tags: ["concept", "area/memory-systems"]
---

# Agent Memory

Where an agent's "memory" lives — context window vs KV cache vs vector store vs database — and how to manage it (retrieval-as-memory, summarization, KV reuse). Context is the scarce resource; this is an unsolved design space.

> [!info] Why it matters for an infra engineer
> Memory architecture trades quality against cost and latency. Choosing where memory lives is one of the open design problems in agent infra.

## Related

- **Area:** [[Memory Systems]]
- **Prerequisites:** [[KV Cache]], [[RAG]], [[Vector Search (HNSW and IVF)]]
- **Unlocks:** [[Multi-Agent and A2A]]
- **Studied in:** [[Week 47 — Memory systems & context engineering]]
- **Resources:** [[qdrant]]
- **Projects:** [[Level 7 — Production-grade AI platform]]

## Notes
