---
type: "week"
week: 18
phase: "Phase 3 — Inference Infrastructure"
status: "not-started"
start: 
end: 
objective: "RAG as a system (and why naive RAG fails): chunking, retrieval, reranking, context assembly."
concepts: ["[[RAG]]"]
project: ["[[Level 2 — RAG with hybrid search & observability]]"]
deliverable: 
tags: ["week", "phase/3"]
---

# Week 18 — RAG as a system

**Phase:** [[Phase 3 — Inference Infrastructure]]  
**Objective:** RAG as a system (and why naive RAG fails): chunking, retrieval, reranking, context assembly.  
**Concepts:** [[RAG]]
**Project:** [[Level 2 — RAG with hybrid search & observability]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
A "RAG is not just top-k" engineering talk; reranker basics.

## Read (15m)
An honest "why our RAG was bad and how we fixed it" postmortem.

## Build (20m)
Build a minimal RAG pipeline (ingest → embed → retrieve → rerank → serve) over your own docs.

## Step-by-step
1. Assemble a small doc corpus and a handful of real questions with known answers.
2. Build the pipeline: ingest → chunk → embed → retrieve top-k → assemble context → generate.
3. Run the questions; for each bad answer, log whether retrieval or generation failed.
4. Vary chunk size and overlap; observe the effect on answer quality.
5. Tally failure attribution: what fraction of errors are retrieval vs generation?

## Reflect (5m)
> Which stage contributes most to bad answers — retrieval or generation? How would you measure it?

## Done when
- [ ] You have a working end-to-end RAG over your own docs.
- [ ] You attributed each failure to retrieval or generation.
- [ ] You can name the stage that contributes most to bad answers, with evidence.

## Common pitfalls
- Bad chunking (splitting mid-thought) silently destroys retrieval quality.
- "The model is dumb" is usually wrong — most RAG failures are retrieval failures.

## Resources
- [[Character.AI, Cursor & Perplexity Engineering]]

## Go deeper
- A "RAG is not just top-k" engineering talk.
- An honest "why our RAG was bad and how we fixed it" postmortem.

## Tasks
- [ ] Study/open [[Character.AI, Cursor & Perplexity Engineering]]
- [ ] **Build:** Build a minimal RAG pipeline (ingest → embed → retrieve → rerank → serve) over your own docs.
- [ ] You have a working end-to-end RAG over your own docs.
- [ ] You attributed each failure to retrieval or generation.
- [ ] You can name the stage that contributes most to bad answers, with evidence.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
