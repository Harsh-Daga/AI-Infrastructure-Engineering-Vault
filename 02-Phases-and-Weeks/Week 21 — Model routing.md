---
type: "week"
week: 21
phase: "Phase 3 — Inference Infrastructure"
status: "not-started"
start: 
end: 
objective: "Model routing (quality/cost/latency-aware): complexity-based routing, cascades, router eval."
concepts: ["[[Model Routing]]", "[[AI Cost Engineering]]"]
project: ["[[Level 3 — Multi-model routing gateway + cost optimization]]"]
deliverable: 
tags: ["week", "phase/3"]
---

# Week 21 — Model routing

**Phase:** [[Phase 3 — Inference Infrastructure]]  
**Objective:** Model routing (quality/cost/latency-aware): complexity-based routing, cascades, router eval.  
**Concepts:** [[Model Routing]], [[AI Cost Engineering]]
**Project:** [[Level 3 — Multi-model routing gateway + cost optimization]]

## Learn (20m)
RouteLLM / routing-research overviews; gateway routing docs.

## Read (15m)
A "how we route between models to cut cost" engineering post.

## Build (20m)
Implement a 2-tier router: small/cheap model first, escalate hard prompts to a big model; measure cost and quality.

## Reflect (5m)
> How do you decide at request time whether a query is "hard"? What signal is cheap and predictive?

## Resources
- [[litellm]]
- [[Character.AI, Cursor & Perplexity Engineering]]

## Tasks
- [ ] Study/open [[litellm]]
- [ ] Study/open [[Character.AI, Cursor & Perplexity Engineering]]
- [ ] **Build:** Implement a 2-tier router: small/cheap model first, escalate hard prompts to a big model; measure cost and quality.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
