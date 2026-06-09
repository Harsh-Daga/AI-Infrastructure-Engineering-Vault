---
type: "week"
week: 8
phase: "Phase 1 — Foundations"
status: "not-started"
start: 
end: 
objective: "Model families & what they cost to run: dense vs MoE, reasoning models (long decode)."
concepts: ["[[Mixture of Experts]]", "[[Reasoning Models]]", "[[Distillation]]", "[[Fine-tuning and RLHF]]", "[[Prefill vs Decode]]", "[[Expert Parallelism]]"]
project: ["[[Level 1 — Run local LLMs]]"]
deliverable: "Phase-1 deliverable: a 1-page \"How an LLM runs on a GPU\" diagram + notes, published to your learning log."
tags: ["week", "phase/1"]
---

# Week 08 — Model families & what they cost to run

**Phase:** [[Phase 1 — Foundations]]  
**Objective:** Model families & what they cost to run: dense vs MoE, reasoning models (long decode).  
**Concepts:** [[Mixture of Experts]], [[Reasoning Models]], [[Distillation]], [[Fine-tuning and RLHF]], [[Prefill vs Decode]], [[Expert Parallelism]]
**Project:** [[Level 1 — Run local LLMs]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
Read about MoE (expert parallelism, all-to-all comms) and reasoning models conceptually.

1. Read about MoE: experts, routing, all-to-all comms, active vs total params.
2. Read about reasoning models and why they decode for a long time.
3. Write how each one shifts the prefill-vs-decode balance.

## Read (15m)
DeepSeek / Llama / Qwen technical reports — only the serving/architecture/efficiency sections.

1. Read the serving/efficiency sections of a DeepSeek/Llama/Qwen tech report.
2. Skip pretraining details; focus on the inference-cost claims.
3. Note active-vs-total params for the MoE model.

## Build (20m)
Run a dense model and an MoE model; compare memory and throughput profiles.

## Step-by-step
1. Run a dense model (e.g. Llama 8B) and capture memory + tokens/sec at fixed batch/context.
2. Run an MoE model (e.g. a Mixtral/Qwen-MoE) at the same settings; compare active vs total params.
3. Run a reasoning model and observe how long the decode phase runs vs a non-reasoning model.
4. Tabulate: total params, active params, VRAM, prefill cost, decode length, tokens/sec.
5. Write the 1-page "How an LLM runs on a GPU" diagram for the Phase-1 deliverable.

## Reflect (5m)
> Why does a reasoning model change your decode-vs-prefill capacity planning?

## Done when
- [ ] You compared dense vs MoE memory and throughput profiles directly.
- [ ] You quantified how a reasoning model shifts work into the decode phase.
- [ ] Phase-1 deliverable published to your learning log.

## Common pitfalls
- MoE VRAM is dominated by all experts even though only a few are active per token.
- Reasoning models can 10× your output tokens — capacity planning must budget decode, not just prefill.

## Resources
- [[Switch Transformer & GShard (MoE)]]
- [[Llama, DeepSeek & Qwen Technical Reports]]

## Go deeper
- DeepSeek/Qwen/Llama technical reports — serving and efficiency sections only.
- An MoE expert-parallelism explainer (all-to-all comms).

## Tasks
- [ ] Study/open [[Switch Transformer & GShard (MoE)]]
- [ ] Study/open [[Llama, DeepSeek & Qwen Technical Reports]]
- [ ] **Build:** Run a dense model and an MoE model; compare memory and throughput profiles.
- [ ] You compared dense vs MoE memory and throughput profiles directly.
- [ ] You quantified how a reasoning model shifts work into the decode phase.
- [ ] Phase-1 deliverable published to your learning log.
- [ ] **Reflect:** answer the week's question in the learning log

## Phase deliverable
> [!success] Phase-1 deliverable: a 1-page "How an LLM runs on a GPU" diagram + notes, published to your learning log.

## Notes
