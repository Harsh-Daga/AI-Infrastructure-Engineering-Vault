---
type: "project"
level: 8
status: "not-started"
phase: "[[Phase 6 — Reliability, Agents, Scale Simulation & Your Specialization]]"
skills: ["[[Cluster Topology]]", "[[InfiniBand vs RoCE]]", "[[NVLink and NVSwitch]]", "[[ZeRO and FSDP]]", "[[Checkpointing and Fault Tolerance]]", "[[AI Cost Engineering]]"]
repos: ["[[Megatron-LM]]"]
success-criteria: "A senior infra engineer reading your doc agrees the design would actually work, and can't find an obvious scaling cliff you didn't address."
tags: ["project", "level/8"]
---

# Level 8 — Frontier-scale architecture simulation

**Phase:** [[Phase 6 — Reliability, Agents, Scale Simulation & Your Specialization]]  
**Weeks:** [[Week 50 — Frontier-scale architecture simulation]]

## Architecture
A *design artifact* (not a running cluster): a complete 10k–100k-GPU training + inference fleet — rail-optimized fabric (IB/RoCE), NVLink/NVSwitch domains, scheduler, storage/checkpoint tiers, disaggregated serving, reliability strategy, and a full cost/capacity model.

## Components
topology diagram, scheduling design, serving design, storage/checkpoint design, failure-handling design, capacity & cost model, and a written defense of every tradeoff.

## Why it matters
Demonstrates you can reason at the scale frontier labs operate — the difference between senior and staff/principal.

## Skills learned
systems design at scale, networking economics, capacity planning, reliability strategy, written technical leadership.

## Skills (concept links)

- [[Cluster Topology]]
- [[InfiniBand vs RoCE]]
- [[NVLink and NVSwitch]]
- [[ZeRO and FSDP]]
- [[Checkpointing and Fault Tolerance]]
- [[AI Cost Engineering]]

## Success criteria
> A senior infra engineer reading your doc agrees the design would actually work, and can't find an obvious scaling cliff you didn't address.

## Repos to study
[[Megatron-LM]] · [[Hugging Face Ultra-Scale Playbook]]

## Build log
_Log progress here as you build._


## Tasks
- [ ] Scaffold the repo with a real README and architecture doc
- [ ] Implement the core architecture above
- [ ] Produce the benchmark / cost model that proves the success criteria
- [ ] Write the "what I learned" section and publish to the learning log
