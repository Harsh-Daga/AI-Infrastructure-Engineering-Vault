---
type: "week"
week: 24
phase: "Phase 3 — Inference Infrastructure"
status: "not-started"
start: 
end: 
objective: "AI cost optimization (the skill that always pays): utilization, quant, routing, caching, spot."
concepts: ["[[AI Cost Engineering]]"]
project: ["[[Level 3 — Multi-model routing gateway + cost optimization]]"]
deliverable: "Phase-3 deliverable: a multi-model gateway + RAG with full observability and a cost model (Project Levels 2–3)."
tags: ["week", "phase/3"]
---

# Week 24 — AI cost optimization

**Phase:** [[Phase 3 — Inference Infrastructure]]  
**Objective:** AI cost optimization (the skill that always pays): utilization, quant, routing, caching, spot.  
**Concepts:** [[AI Cost Engineering]]
**Project:** [[Level 3 — Multi-model routing gateway + cost optimization]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
A GPU cost-optimization playbook; cloud GPU pricing vs bare-metal economics.

1. Read a GPU cost-optimization playbook.
2. Compare cloud GPU pricing vs bare-metal economics.
3. List the levers: size, quant, routing, batching, scheduling, spot.

## Read (15m)
A "how we cut our inference bill 60%" engineering writeup.

1. Read a "how we cut inference cost 60%" writeup.
2. Note their single biggest lever.
3. Write the $ impact they claimed.

## Build (20m)
Take one of your deployments and produce a documented cost-reduction plan (model size, quant, routing, batching, scheduling) with projected $ impact.

## Step-by-step
1. Pick one of your deployments and compute current cost-per-token (or per-request).
2. Enumerate levers: model size, quantization, routing, batching, scheduling, spot/bare-metal.
3. Estimate the $ impact of each lever and stack-rank them.
4. Apply the top lever, re-measure, and confirm the projected saving.
5. Write the Phase-3 deliverable: gateway + RAG + observability + a cost model.

## Reflect (5m)
> What's the single biggest lever on cost-per-token for your workload?

## Done when
- [ ] A documented cost-reduction plan with projected $ impact per lever.
- [ ] At least one lever applied and verified.
- [ ] Phase-3 deliverable assembled (Project Levels 2–3).

## Common pitfalls
- Optimizing cost without an eval can quietly tank quality — gate every change on eval.
- Spot/preemptible saves money only if your system tolerates eviction.

## Resources
- [[SemiAnalysis]]
- [[Character.AI, Cursor & Perplexity Engineering]]

## Go deeper
- A GPU cost-optimization playbook; cloud GPU vs bare-metal economics.
- A "how we cut our inference bill 60%" writeup.

## Tasks
- [ ] Study/open [[SemiAnalysis]]
- [ ] Study/open [[Character.AI, Cursor & Perplexity Engineering]]
- [ ] **Build:** Take one of your deployments and produce a documented cost-reduction plan (model size, quant, routing, batching, scheduling) with projected $ impact.
- [ ] A documented cost-reduction plan with projected $ impact per lever.
- [ ] At least one lever applied and verified.
- [ ] Phase-3 deliverable assembled (Project Levels 2–3).
- [ ] **Reflect:** answer the week's question in the learning log

## Phase deliverable
> [!success] Phase-3 deliverable: a multi-model gateway + RAG with full observability and a cost model (Project Levels 2–3).

## Notes
