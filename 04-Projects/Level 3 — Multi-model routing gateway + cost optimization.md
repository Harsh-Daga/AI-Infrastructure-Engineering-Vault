---
type: "project"
level: 3
status: "not-started"
phase: "[[Phase 3 — Inference Infrastructure]]"
skills: ["[[AI Gateway]]", "[[Model Routing]]", "[[AI Cost Engineering]]", "[[Quantization]]", "[[OTel GenAI Conventions]]"]
repos: ["[[litellm]]", "[[ai-gateway]]", "[[Portkey-gateway]]"]
success-criteria: "Demonstrate a measured cost reduction (e.g. 30–60%) at held quality via routing + quantization + caching, with a before/after cost model."
tags: ["project", "level/3"]
---

# Level 3 — Multi-model routing gateway + cost optimization

**Phase:** [[Phase 3 — Inference Infrastructure]]  
**Weeks:** [[Week 20 — AI gateways — the multi-model edge]], [[Week 21 — Model routing]], [[Week 24 — AI cost optimization]]

## Architecture
LiteLLM (or Envoy AI Gateway) fronting self-hosted vLLM + ≥1 hosted API, with a complexity-based router, budgets, failover, and guardrails.

## Components
gateway, virtual keys/budgets, a 2-tier router (cheap→escalate), OTel export, a cost dashboard.

## Why it matters
The multi-model edge is the everyday control point of a real AI platform; routing + cost is where you save real money.

## Skills learned
gateway ops, model routing, failover, budget enforcement, cost modeling, semantic guardrails.

## Skills (concept links)

- [[AI Gateway]]
- [[Model Routing]]
- [[AI Cost Engineering]]
- [[Quantization]]
- [[OTel GenAI Conventions]]

## Success criteria
> Demonstrate a measured cost reduction (e.g. 30–60%) at held quality via routing + quantization + caching, with a before/after cost model.

## Repos to study
[[litellm]], [[ai-gateway]], [[Portkey-gateway]]

## Build log
_Log progress here as you build._


## Tasks
- [ ] Scaffold the repo with a real README and architecture doc
- [ ] Implement the core architecture above
- [ ] Produce the benchmark / cost model that proves the success criteria
- [ ] Write the "what I learned" section and publish to the learning log
