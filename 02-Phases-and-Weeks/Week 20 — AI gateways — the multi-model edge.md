---
type: "week"
week: 20
phase: "Phase 3 — Inference Infrastructure"
status: "not-started"
start: 
end: 
objective: "AI gateways — the multi-model edge: virtual keys, budgets, failover, guardrails."
concepts: ["[[AI Gateway]]", "[[Model Routing]]"]
project: ["[[Level 3 — Multi-model routing gateway + cost optimization]]"]
deliverable: 
tags: ["week", "phase/3"]
---

# Week 20 — AI gateways — the multi-model edge

**Phase:** [[Phase 3 — Inference Infrastructure]]  
**Objective:** AI gateways — the multi-model edge: virtual keys, budgets, failover, guardrails.  
**Concepts:** [[AI Gateway]], [[Model Routing]]
**Project:** [[Level 3 — Multi-model routing gateway + cost optimization]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
LiteLLM docs; Portkey/Kong AI Gateway/Envoy AI Gateway overviews.

1. Read LiteLLM docs; skim Portkey/Kong/Envoy AI Gateway overviews.
2. Learn virtual keys, budgets, failover, and guardrails.
3. Write what belongs at the gateway vs inside each service.

## Read (15m)
A 2026 AI-gateway comparison (LiteLLM vs Portkey vs Kong) and the security notes (e.g. supply-chain incidents).

1. Read a 2026 AI-gateway comparison including the security notes.
2. Note a real supply-chain incident it mentions.
3. Write the gateway's single-point-of-failure risk.

## Build (20m)
Deploy LiteLLM in front of your vLLM endpoint + one hosted API; add a virtual key with a budget cap and a failover route.

## Step-by-step
1. Deploy LiteLLM in front of your vLLM endpoint plus one hosted API (e.g. an Anthropic/OpenAI key).
2. Create a virtual key with a budget cap and per-model rate limits.
3. Configure a failover route: primary model down → fall back to secondary.
4. Test it: exhaust the budget and kill the primary; confirm cap enforcement and failover.
5. Decide what logic belongs at the gateway vs inside each service.

## Reflect (5m)
> What belongs at the gateway vs inside each service? Where does the gateway become a bottleneck or SPOF?

## Done when
- [ ] Virtual key with a working budget cap and rate limit.
- [ ] Verified automatic failover when the primary is unavailable.
- [ ] You can articulate the gateway's SPOF/bottleneck risks.

## Common pitfalls
- The gateway becomes a single point of failure — plan its HA before it's load-bearing.
- Per-key budgets need a shared store (e.g. Redis) to be correct across replicas.

## Resources
- [[litellm]]
- [[ai-gateway]]
- [[Portkey-gateway]]
- [[Cloudflare Blog]]

## Go deeper
- LiteLLM docs; Portkey / Kong AI Gateway / Envoy AI Gateway overviews.
- A 2026 AI-gateway comparison incl. supply-chain security notes.

## Tasks
- [ ] Study/open [[litellm]]
- [ ] Study/open [[ai-gateway]]
- [ ] Study/open [[Portkey-gateway]]
- [ ] Study/open [[Cloudflare Blog]]
- [ ] **Build:** Deploy LiteLLM in front of your vLLM endpoint + one hosted API; add a virtual key with a budget cap and a failover route.
- [ ] Virtual key with a working budget cap and rate limit.
- [ ] Verified automatic failover when the primary is unavailable.
- [ ] You can articulate the gateway's SPOF/bottleneck risks.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
