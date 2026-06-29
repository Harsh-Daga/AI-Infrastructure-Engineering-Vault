---
type: week
week: 3
phase: Phase 1 — Foundations
status: done
start: 2026-06-14
end: 29/06/2026
objective: "Attention & the transformer through an infra lens: shapes and memory cost, not gradient math."
concepts:
  - "[[Attention]]"
  - "[[Transformer Block]]"
project:
  - "[[Level 1 — Run local LLMs]]"
deliverable:
tags:
  - week
  - phase/1
---

# Week 03 — Attention & the transformer, infra lens

**Phase:** [[Phase 1 — Foundations]]  
**Objective:** Attention & the transformer through an infra lens: shapes and memory cost, not gradient math.  
**Concepts:** [[Attention]], [[Transformer Block]]
**Project:** [[Level 1 — Run local LLMs]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
3Blue1Brown "Attention in transformers" + "But what is a GPT?" (visual, intuition-first).

1. Watch 3Blue1Brown "Attention in transformers" for the QKV intuition.
2. Then "But what is a GPT?" for the end-to-end flow; pause on the matrix shapes.
3. Write what attention computes and which tensors scale with sequence length.

## Read (15m)
"Attention Is All You Need" — read the architecture section only; ignore the training math.

1. Read only the architecture section of "Attention Is All You Need"; skip the training math.
2. Identify the per-layer components (attention, MLP, residual, norm).
3. Note which buffers must persist across decode steps (the KV).

## Build (20m)
Run a model at increasing context lengths; measure VRAM growth. Plot memory vs context.

## Step-by-step
1. Serve or run one model locally with a long-context build.
2. Send prompts at increasing context lengths (e.g. 1k, 4k, 16k, 32k tokens) and capture VRAM after each.
3. Plot VRAM vs context length; identify the linear KV-cache growth term vs the fixed weights term.
4. Re-read the Transformer architecture diagram and label which tensors grow with sequence length.

## Reflect (5m)
> What part of memory grows with context length, and what does that imply for serving?

## Done when
- [x] You have a memory-vs-context plot for one model.
- [x] You can separate fixed (weights) from context-dependent (KV) memory.
- [x] You can explain why attention is O(n²) compute but the KV cache is O(n) memory.

## Common pitfalls
- Allocator caching can mask true growth — measure peak, and reset between runs.
- Quantized weights shrink the fixed term but not the KV term; keep them separate.

## Resources
- [[3Blue1Brown — Neural Networks series]]
- [[Attention Is All You Need]]
- [[Jay Alammar — The Illustrated Transformer]]

## Go deeper
- 3Blue1Brown "Attention in transformers" — the visual intuition for QKV.
- The Illustrated Transformer (Jay Alammar) — shapes, not gradients.

## Tasks
- [x] Study/open [[3Blue1Brown — Neural Networks series]]
- [x] Study/open [[Attention Is All You Need]]
- [x] Study/open [[Jay Alammar — The Illustrated Transformer]]
- [x] **Build:** Run a model at increasing context lengths; measure VRAM growth. Plot memory vs context.
- [x] You have a memory-vs-context plot for one model.
- [x] You can separate fixed (weights) from context-dependent (KV) memory.
- [x] You can explain why attention is O(n²) compute but the KV cache is O(n) memory.
- [x] **Reflect:** answer the week's question in the learning log

## Notes
