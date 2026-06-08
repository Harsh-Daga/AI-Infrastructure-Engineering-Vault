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

## Learn (20m)
Read about MoE (expert parallelism, all-to-all comms) and reasoning models conceptually.

## Read (15m)
DeepSeek / Llama / Qwen technical reports — only the serving/architecture/efficiency sections.

## Build (20m)
Run a dense model and an MoE model; compare memory and throughput profiles.

## Reflect (5m)
> Why does a reasoning model change your decode-vs-prefill capacity planning?

## Resources
- [[Switch Transformer & GShard (MoE)]]
- [[Llama, DeepSeek & Qwen Technical Reports]]

## Tasks
- [ ] Study/open [[Switch Transformer & GShard (MoE)]]
- [ ] Study/open [[Llama, DeepSeek & Qwen Technical Reports]]
- [ ] **Build:** Run a dense model and an MoE model; compare memory and throughput profiles.
- [ ] **Reflect:** answer the week's question in the learning log

## Phase deliverable
> [!success] Phase-1 deliverable: a 1-page "How an LLM runs on a GPU" diagram + notes, published to your learning log.

## Notes
