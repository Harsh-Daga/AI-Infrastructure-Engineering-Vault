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

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
RouteLLM / routing-research overviews; gateway routing docs.

## Read (15m)
A "how we route between models to cut cost" engineering post.

## Build (20m)
Implement a 2-tier router: small/cheap model first, escalate hard prompts to a big model; measure cost and quality.

## Step-by-step
1. Define two tiers: a small/cheap model and a large/expensive one.
2. Implement a router that sends easy prompts to the small model and escalates hard ones.
3. Choose a cheap difficulty signal (length, keyword/heuristic, or a tiny classifier).
4. Run a mixed prompt set; measure cost, latency, and quality vs always-big and always-small.
5. Tune the escalation threshold to hit a target quality at minimum cost.

## Reflect (5m)
> How do you decide at request time whether a query is "hard"? What signal is cheap and predictive?

## Done when
- [ ] A working 2-tier router with a measured cost/quality tradeoff.
- [ ] You identified a cheap, predictive difficulty signal.
- [ ] You can show the cost saved at a fixed quality bar.

## Common pitfalls
- A bad router that mis-escalates can cost more than always using the big model.
- Routing on the answer (not the prompt) defeats the purpose — decide before generating.

## Resources
- [[litellm]]
- [[Character.AI, Cursor & Perplexity Engineering]]

## Go deeper
- RouteLLM / routing-research overviews.
- A "how we route between models to cut cost" engineering post.

## Tasks
- [ ] Study/open [[litellm]]
- [ ] Study/open [[Character.AI, Cursor & Perplexity Engineering]]
- [ ] **Build:** Implement a 2-tier router: small/cheap model first, escalate hard prompts to a big model; measure cost and quality.
- [ ] A working 2-tier router with a measured cost/quality tradeoff.
- [ ] You identified a cheap, predictive difficulty signal.
- [ ] You can show the cost saved at a fixed quality bar.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
