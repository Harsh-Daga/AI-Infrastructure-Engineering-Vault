---
type: "week"
week: 13
phase: "Phase 2 — LLM Serving, Deep"
status: "not-started"
start: 
end: 
objective: "Speculative decoding & advanced latency tricks: draft models, medusa/eagle, chunked prefill."
concepts: ["[[Speculative Decoding]]"]
project: []
deliverable: 
tags: ["week", "phase/2"]
---

# Week 13 — Speculative decoding & latency tricks

**Phase:** [[Phase 2 — LLM Serving, Deep]]  
**Objective:** Speculative decoding & advanced latency tricks: draft models, medusa/eagle, chunked prefill.  
**Concepts:** [[Speculative Decoding]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
A speculative-decoding explainer; vLLM/SGLang spec-decode docs.

## Read (15m)
The speculative decoding paper (concept + results sections).

## Build (20m)
Enable speculative decoding; measure tokens/sec uplift and any quality/acceptance-rate cost.

## Step-by-step
1. Pick a target model and a smaller draft model (or a built-in EAGLE/Medusa head).
2. Enable speculative decoding in vLLM/SGLang and serve.
3. Measure tokens/sec and the draft acceptance rate vs the non-speculative baseline.
4. Vary prompt types (code, prose, math) and watch acceptance rate move.
5. Compute net speedup vs extra compute spent on rejected draft tokens.

## Reflect (5m)
> Why is speculative decoding "free" throughput sometimes and wasted compute other times?

## Done when
- [ ] You measured tokens/sec uplift and acceptance rate.
- [ ] You found a workload where speculation helps and one where it doesn't.
- [ ] You can explain when speculation is free throughput vs wasted compute.

## Common pitfalls
- Low acceptance rate means you pay draft compute for little gain — it can be net-negative.
- Output must match the target model's distribution; verify quality didn't drift.

## Resources
- [[Speculative Decoding]]
- [[SGLang Documentation]]
- [[vLLM Documentation]]

## Go deeper
- The speculative decoding paper (concept + results).
- vLLM/SGLang spec-decode docs (draft models, EAGLE, Medusa).

## Tasks
- [ ] Study/open [[Speculative Decoding]]
- [ ] Study/open [[SGLang Documentation]]
- [ ] Study/open [[vLLM Documentation]]
- [ ] **Build:** Enable speculative decoding; measure tokens/sec uplift and any quality/acceptance-rate cost.
- [ ] You measured tokens/sec uplift and acceptance rate.
- [ ] You found a workload where speculation helps and one where it doesn't.
- [ ] You can explain when speculation is free throughput vs wasted compute.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
