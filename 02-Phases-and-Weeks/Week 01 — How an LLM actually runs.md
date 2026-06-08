---
type: "week"
week: 1
phase: "Phase 1 — Foundations"
status: "in-progress"
start: "2026-06-09"
end: 
objective: "Build the 10,000-ft systems view of how an LLM runs: tokens, prefill → decode, where GPU time goes."
concepts: ["[[Tokenization]]", "[[Prefill vs Decode]]", "[[TTFT vs ITL]]"]
project: ["[[Level 1 — Run local LLMs]]"]
deliverable: 
tags: ["week", "phase/1"]
---

# Week 01 — How an LLM actually runs

**Phase:** [[Phase 1 — Foundations]]  
**Objective:** Build the 10,000-ft systems view of how an LLM runs: tokens, prefill → decode, where GPU time goes.  
**Concepts:** [[Tokenization]], [[Prefill vs Decode]], [[TTFT vs ITL]]
**Project:** [[Level 1 — Run local LLMs]]

## Learn (20m)
Andrej Karpathy "Let's build the GPT Tokenizer" + "Intro to LLMs" (1hr talk) — watch the systems-relevant parts.

## Read (15m)
Jay Alammar, "The Illustrated Transformer" (skim for shapes, not math).

## Build (20m)
Install Ollama; run a small model (e.g. Llama 3.x 8B). Time first-token vs full-response. Log GPU/CPU/RAM.

## Reflect (5m)
> Where does latency come from before the first token vs between tokens? Why?

## Resources
- [[Karpathy — Neural Networks Zero to Hero]]
- [[Andrej Karpathy (YouTube)]]
- [[Jay Alammar — The Illustrated Transformer]]
- [[ollama]]

## Tasks
- [ ] Study/open [[Karpathy — Neural Networks Zero to Hero]]
- [ ] Study/open [[Andrej Karpathy (YouTube)]]
- [ ] Study/open [[Jay Alammar — The Illustrated Transformer]]
- [ ] Study/open [[ollama]]
- [ ] **Build:** Install Ollama; run a small model (e.g. Llama 3.x 8B). Time first-token vs full-response. Log GPU/CPU/RAM.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
