---
type: "week"
week: 23
phase: "Phase 3 — Inference Infrastructure"
status: "not-started"
start: 
end: 
objective: "Evaluation as infrastructure: offline eval sets, LLM-as-judge, regression testing (CI for quality)."
concepts: ["[[Eval as Infrastructure]]"]
project: []
deliverable: 
tags: ["week", "phase/3"]
---

# Week 23 — Evaluation as infrastructure

**Phase:** [[Phase 3 — Inference Infrastructure]]  
**Objective:** Evaluation as infrastructure: offline eval sets, LLM-as-judge, regression testing (CI for quality).  
**Concepts:** [[Eval as Infrastructure]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
An eval-infra talk (e.g. Braintrust/OpenAI evals/Phoenix evals).

1. Watch an eval-infra talk (Braintrust / OpenAI evals / Phoenix).
2. Learn offline eval sets, LLM-as-judge, and regression gating.
3. Write the rubric you'll score against.

## Read (15m)
"Your eval is your moat" style engineering posts.

1. Read a "your eval is your moat" post.
2. Note the judge biases they warn about.
3. Write how they keep the eval set from being gamed.

## Build (20m)
Build a small eval harness that scores your RAG/router against a fixed set on every change (CI for quality).

## Step-by-step
1. Curate a fixed eval set (inputs + reference answers or rubrics) for your RAG/router.
2. Implement scorers: exact/semantic match where possible, plus an LLM-as-judge with a rubric.
3. Wire the eval to run on every change (a script or CI job) and emit a score.
4. Make a deliberate prompt tweak and watch the eval catch (or miss) the regression.
5. Calibrate the judge against a few human labels to check it's trustworthy.

## Reflect (5m)
> How do you stop a "small prompt tweak" from silently regressing quality in prod?

## Done when
- [ ] An eval harness that scores on every change (CI for quality).
- [ ] You demonstrated it catching a regression.
- [ ] You calibrated the LLM-judge against human labels.

## Common pitfalls
- LLM-as-judge is biased (position, verbosity, self-preference) — calibrate and randomize.
- An eval set that never changes gets gamed; refresh it as failure modes appear.

## Resources
- [[phoenix]]
- [[langfuse]]

## Go deeper
- An eval-infra talk (Braintrust / OpenAI evals / Phoenix evals).
- "Your eval is your moat" engineering posts.

## Tasks
- [ ] Study/open [[phoenix]]
- [ ] Study/open [[langfuse]]
- [ ] **Build:** Build a small eval harness that scores your RAG/router against a fixed set on every change (CI for quality).
- [ ] An eval harness that scores on every change (CI for quality).
- [ ] You demonstrated it catching a regression.
- [ ] You calibrated the LLM-judge against human labels.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
