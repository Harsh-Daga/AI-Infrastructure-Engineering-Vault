---
type: "week"
week: 9
phase: "Phase 2 — LLM Serving, Deep"
status: "not-started"
start: 
end: 
objective: "Serving fundamentals: static vs dynamic vs continuous batching, throughput/latency tradeoff, admission control."
concepts: ["[[Continuous Batching]]", "[[TTFT vs ITL]]", "[[Queueing and Backpressure]]"]
project: []
deliverable: 
tags: ["week", "phase/2"]
---

# Week 09 — Serving fundamentals — batching

**Phase:** [[Phase 2 — LLM Serving, Deep]]  
**Objective:** Serving fundamentals: static vs dynamic vs continuous batching, throughput/latency tradeoff, admission control.  
**Concepts:** [[Continuous Batching]], [[TTFT vs ITL]], [[Queueing and Backpressure]]

## Learn (20m)
Anyscale "Continuous batching" blog; vLLM docs (architecture).

## Read (15m)
The Orca / continuous-batching writeups; vLLM design docs.

## Build (20m)
Load-test a vLLM endpoint (e.g. with `vllm bench` or a `locust`/`k6` script) at 1, 10, 50 concurrent users; chart TTFT and throughput.

## Reflect (5m)
> Why does TTFT explode under concurrency on a naive setup, and how does continuous batching help?

## Resources
- [[Anyscale — Continuous Batching Blog]]
- [[vLLM Documentation]]

## Tasks
- [ ] Study/open [[Anyscale — Continuous Batching Blog]]
- [ ] Study/open [[vLLM Documentation]]
- [ ] **Build:** Load-test a vLLM endpoint (e.g. with `vllm bench` or a `locust`/`k6` script) at 1, 10, 50 concurrent users; chart TTFT and throughput.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
