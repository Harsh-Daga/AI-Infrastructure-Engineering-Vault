---
type: "phase"
phase: 1
weeks: "1-8"
status: "not-started"
tags: ["phase", "phase/1"]
---

# Phase 1 — Foundations

> Build the minimum-viable mental model of LLMs and GPUs so the rest of the roadmap is comprehensible. Aggressively infra-flavored.

**Weeks:** 1–8  
**Phase deliverable lands in:** [[Week 08 — Model families & what they cost to run]]

## Projects in this phase

- [[Level 1 — Run local LLMs]]

## Weeks

- [[Week 01 — How an LLM actually runs]]
- [[Week 02 — Tokenization, embeddings, context windows]]
- [[Week 03 — Attention & the transformer, infra lens]]
- [[Week 04 — The KV cache]]
- [[Week 05 — GPU architecture & memory hierarchy]]
- [[Week 06 — Precision & quantization]]
- [[Week 07 — Where the GPU time goes — profiling]]
- [[Week 08 — Model families & what they cost to run]]

## Progress (Dataview)
<!-- Requires Dataview. Shows the status of every week in this phase. -->
```dataview
TABLE status, objective
FROM #week
WHERE phase = "Phase 1 — Foundations"
SORT week ASC
```
