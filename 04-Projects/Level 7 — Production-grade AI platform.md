---
type: "project"
level: 7
status: "not-started"
phase: "[[Phase 6 — Reliability, Agents, Scale Simulation & Your Specialization]]"
skills: ["[[AI Reliability Engineering]]", "[[Eval as Infrastructure]]", "[[Durable Execution]]", "[[AI Cost Engineering]]", "[[Multi-Agent and A2A]]", "[[Agent Memory]]"]
repos: ["[[temporal]]", "[[restate]]", "[[langfuse]]"]
success-criteria: "Documented SLOs + error budgets; chaos tests pass with graceful degradation; a quality-regression alert fires on a bad deploy; a cost model leadership could act on."
tags: ["project", "level/7"]
---

# Level 7 — Production-grade AI platform

**Phase:** [[Phase 6 — Reliability, Agents, Scale Simulation & Your Specialization]]  
**Weeks:** [[Week 31 — The internal AI platform (paved road)]], [[Week 43 — AI reliability engineering — SLOs & error budgets]], [[Week 44 — Failure injection & chaos for AI]], [[Week 45 — Agent infrastructure & durable execution]], [[Week 46 — MCP — building & operating servers]], [[Week 47 — Memory systems & context engineering]], [[Week 48 — Multi-agent infrastructure]], [[Week 49 — AI security & supply chain]], [[Week 52 — Consolidate, publish, and go public]]

## Architecture
Level 4 + Level 6 hardened for production: SLOs + error budgets, chaos/failure injection, eval-as-CI, security/guardrails, multi-tenancy, durable agent execution, and a documented cost model.

## Components
everything above + alerting on quality, load-shedding/fallback, supply-chain hardening, durable-execution layer (Temporal/Restate), runbooks.

## Why it matters
This is the staff-engineer deliverable — not "it works" but "it works under failure, at cost, with SLOs."

## Skills learned
AI reliability engineering, chaos for AI, security, durable execution, the full operational picture.

## Skills (concept links)

- [[AI Reliability Engineering]]
- [[Eval as Infrastructure]]
- [[Durable Execution]]
- [[AI Cost Engineering]]
- [[Multi-Agent and A2A]]
- [[Agent Memory]]

## Success criteria
> Documented SLOs + error budgets; chaos tests pass with graceful degradation; a quality-regression alert fires on a bad deploy; a cost model leadership could act on.

## Repos to study
[[temporal]], [[restate]], [[langfuse]]

## Build log
_Log progress here as you build._


## Tasks
- [ ] Scaffold the repo with a real README and architecture doc
- [ ] Implement the core architecture above
- [ ] Produce the benchmark / cost model that proves the success criteria
- [ ] Write the "what I learned" section and publish to the learning log
