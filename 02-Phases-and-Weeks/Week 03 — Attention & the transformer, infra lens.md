---
type: "week"
week: 3
phase: "Phase 1 — Foundations"
status: "not-started"
start: 
end: 
objective: "Attention & the transformer through an infra lens: shapes and memory cost, not gradient math."
concepts: ["[[Attention]]", "[[Transformer Block]]"]
project: ["[[Level 1 — Run local LLMs]]"]
deliverable: 
tags: ["week", "phase/1"]
---

# Week 03 — Attention & the transformer, infra lens

**Phase:** [[Phase 1 — Foundations]]  
**Objective:** Attention & the transformer through an infra lens: shapes and memory cost, not gradient math.  
**Concepts:** [[Attention]], [[Transformer Block]]
**Project:** [[Level 1 — Run local LLMs]]

## Learn (20m)
3Blue1Brown "Attention in transformers" + "But what is a GPT?" (visual, intuition-first).

## Read (15m)
"Attention Is All You Need" — read the architecture section only; ignore the training math.

## Build (20m)
Run a model at increasing context lengths; measure VRAM growth. Plot memory vs context.

## Reflect (5m)
> What part of memory grows with context length, and what does that imply for serving?

## Resources
- [[3Blue1Brown — Neural Networks series]]
- [[Attention Is All You Need]]
- [[Jay Alammar — The Illustrated Transformer]]

## Tasks
- [ ] Study/open [[3Blue1Brown — Neural Networks series]]
- [ ] Study/open [[Attention Is All You Need]]
- [ ] Study/open [[Jay Alammar — The Illustrated Transformer]]
- [ ] **Build:** Run a model at increasing context lengths; measure VRAM growth. Plot memory vs context.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
