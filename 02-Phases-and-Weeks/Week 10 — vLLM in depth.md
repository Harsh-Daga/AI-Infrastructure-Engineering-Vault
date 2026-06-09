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

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
vLLM official docs end-to-end; a recent vLLM deep-dive talk.

## Read (15m)
vLLM GitHub issues/discussions on production tuning (real-world failure modes).

## Build (20m)
Serve a 7–8B model with vLLM; tune `max-num-seqs`, `gpu-memory-utilization`, `max-model-len`; record the throughput/latency frontier.

## Step-by-step
1. Serve a 7–8B model with vLLM at default settings; record the baseline throughput/latency.
2. Sweep `--max-num-seqs` (e.g. 64/128/256) and record throughput and TTFT at each.
3. Sweep `--gpu-memory-utilization` (e.g. 0.85/0.90/0.95) and watch KV headroom vs OOM risk.
4. Set `--max-model-len` to your real workload's max; note the KV-cache and admission impact.
5. Build the throughput/latency frontier (Pareto curve) and mark your chosen operating point.

## Reflect (5m)
> Which single knob moved your throughput most, and what did it cost?

## Done when
- [ ] You have a Pareto frontier of throughput vs latency across knob settings.
- [ ] You can name the single knob that moved throughput most and its cost.
- [ ] You recorded a recommended config for your workload.

## Common pitfalls
- Pushing `gpu-memory-utilization` to 0.97 maximizes KV but risks OOM under bursty load.
- Higher `max-num-seqs` helps throughput but can hurt TTFT — it's a tradeoff, not a win.

## Resources
- [[vLLM Documentation]]
- [[vllm]]
- [[vLLM Blog]]

## Go deeper
- vLLM production-tuning GitHub discussions — real failure modes.
- A recent vLLM architecture deep-dive talk.

## Tasks
- [ ] Study/open [[vLLM Documentation]]
- [ ] Study/open [[vllm]]
- [ ] Study/open [[vLLM Blog]]
- [ ] **Build:** Serve a 7–8B model with vLLM; tune `max-num-seqs`, `gpu-memory-utilization`, `max-model-len`; record the throughput/latency frontier.
- [ ] You have a Pareto frontier of throughput vs latency across knob settings.
- [ ] You can name the single knob that moved throughput most and its cost.
- [ ] You recorded a recommended config for your workload.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
