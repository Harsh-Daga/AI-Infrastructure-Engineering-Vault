---
type: "project"
level: 6
status: "not-started"
phase: "[[Phase 5 — Networking, Distributed Systems for AI, Distributed Training]]"
skills: ["[[Disaggregated Serving]]", "[[KV Routing]]", "[[KV Offload]]", "[[Collective Communication (NCCL)]]", "[[RDMA]]", "[[Inference Autoscaling]]"]
repos: ["[[dynamo]]", "[[llm-d]]", "[[sglang]]", "[[vllm]]"]
success-criteria: "Demonstrate higher throughput/lower TTFT than aggregated serving on a long-context or reasoning workload; survive a worker failure with graceful recovery; explain the xPyD ratio you chose and why."
tags: ["project", "level/6"]
---

# Level 6 — Distributed inference cluster

**Phase:** [[Phase 5 — Networking, Distributed Systems for AI, Distributed Training]]  
**Weeks:** [[Week 30 — Disaggregated serving — Dynamo & llm-d]], [[Week 42 — Distributed inference at scale]]

## Architecture
Multi-node disaggregated serving with NVIDIA Dynamo (or llm-d): separate prefill/decode pools, KV-aware routing, NIXL KV transport, service discovery, independent autoscaling.

## Components
prefill workers, decode workers, router, KV transport, discovery service, per-pool autoscaling, full tracing.

## Why it matters
Disaggregation is the defining inference architecture of 2026; building it hands-on is rare and immediately credible.

## Skills learned
disaggregated serving, KV transfer over RDMA/NVLink, distributed routing/discovery, multi-pool autoscaling, distributed-systems failure handling.

## Skills (concept links)

- [[Disaggregated Serving]]
- [[KV Routing]]
- [[KV Offload]]
- [[Collective Communication (NCCL)]]
- [[RDMA]]
- [[Inference Autoscaling]]

## Success criteria
> Demonstrate higher throughput/lower TTFT than aggregated serving on a long-context or reasoning workload; survive a worker failure with graceful recovery; explain the xPyD ratio you chose and why.

## Repos to study
[[dynamo]], [[llm-d]], [[sglang]], [[vllm]]

## Build log
_Log progress here as you build._


## Tasks
- [ ] Scaffold the repo with a real README and architecture doc
- [ ] Implement the core architecture above
- [ ] Produce the benchmark / cost model that proves the success criteria
- [ ] Write the "what I learned" section and publish to the learning log
