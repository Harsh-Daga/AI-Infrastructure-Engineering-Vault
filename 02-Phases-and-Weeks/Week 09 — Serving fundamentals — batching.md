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

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
Anyscale "Continuous batching" blog; vLLM docs (architecture).

1. Read the Anyscale continuous-batching blog for the core idea.
2. Skim the vLLM architecture docs for the scheduler.
3. Write why static batching wastes the GPU and iteration-level scheduling fixes it.

## Read (15m)
The Orca / continuous-batching writeups; vLLM design docs.

1. Read the Orca / continuous-batching writeups.
2. Note the difference between request-level and iteration-level batching.
3. Write what admission control protects against.

## Build (20m)
Load-test a vLLM endpoint (e.g. with `vllm bench` or a `locust`/`k6` script) at 1, 10, 50 concurrent users; chart TTFT and throughput.

## Step-by-step
1. Serve a model with vLLM (`vllm serve <model>`) and expose the OpenAI-compatible endpoint.
2. Write a load script (`vllm bench`, `locust`, or `k6`) and run at 1, 10, then 50 concurrent users.
3. At each level capture TTFT (p50/p95), end-to-end latency, and total throughput (tokens/sec).
4. Plot TTFT and throughput vs concurrency; find where TTFT starts to blow up.
5. Toggle a naive (no continuous batching) baseline if available and compare the curves.

## Reflect (5m)
> Why does TTFT explode under concurrency on a naive setup, and how does continuous batching help?

## Done when
- [ ] You have TTFT-and-throughput-vs-concurrency curves.
- [ ] You can explain why throughput rises while TTFT degrades under load.
- [ ] You can articulate what continuous batching changes about the curve.

## Common pitfalls
- Client-side bottlenecks (single-threaded load gen) cap measured throughput — verify the client isn't the limit.
- Cold cache / first requests skew p95 — discard a warmup window.

## Resources
- [[Anyscale — Continuous Batching Blog]]
- [[vLLM Documentation]]

## Go deeper
- Anyscale "Continuous batching" blog.
- The Orca paper — iteration-level scheduling, the idea behind continuous batching.

## Tasks
- [ ] Study/open [[Anyscale — Continuous Batching Blog]]
- [ ] Study/open [[vLLM Documentation]]
- [ ] **Build:** Load-test a vLLM endpoint (e.g. with `vllm bench` or a `locust`/`k6` script) at 1, 10, 50 concurrent users; chart TTFT and throughput.
- [ ] You have TTFT-and-throughput-vs-concurrency curves.
- [ ] You can explain why throughput rises while TTFT degrades under load.
- [ ] You can articulate what continuous batching changes about the curve.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
