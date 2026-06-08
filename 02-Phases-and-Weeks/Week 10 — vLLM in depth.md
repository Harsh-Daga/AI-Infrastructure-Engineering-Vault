---
type: "week"
week: 10
phase: "Phase 2 — LLM Serving, Deep"
status: "not-started"
start: 
end: 
objective: "vLLM in depth: PagedAttention internals, scheduler, tensor parallelism, knobs."
concepts: ["[[PagedAttention]]", "[[Tensor Parallelism]]", "[[Continuous Batching]]"]
project: []
deliverable: 
tags: ["week", "phase/2"]
---

# Week 10 — vLLM in depth

**Phase:** [[Phase 2 — LLM Serving, Deep]]  
**Objective:** vLLM in depth: PagedAttention internals, scheduler, tensor parallelism, knobs.  
**Concepts:** [[PagedAttention]], [[Tensor Parallelism]], [[Continuous Batching]]

## Learn (20m)
vLLM official docs end-to-end; a recent vLLM deep-dive talk.

## Read (15m)
vLLM GitHub issues/discussions on production tuning (real-world failure modes).

## Build (20m)
Serve a 7–8B model with vLLM; tune `max-num-seqs`, `gpu-memory-utilization`, `max-model-len`; record the throughput/latency frontier.

## Reflect (5m)
> Which single knob moved your throughput most, and what did it cost?

## Resources
- [[vLLM Documentation]]
- [[vllm]]
- [[vLLM Blog]]

## Tasks
- [ ] Study/open [[vLLM Documentation]]
- [ ] Study/open [[vllm]]
- [ ] Study/open [[vLLM Blog]]
- [ ] **Build:** Serve a 7–8B model with vLLM; tune `max-num-seqs`, `gpu-memory-utilization`, `max-model-len`; record the throughput/latency frontier.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
