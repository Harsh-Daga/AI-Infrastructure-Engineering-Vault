---
type: "week"
week: 49
phase: "Phase 6 — Reliability, Agents, Scale Simulation & Your Specialization"
status: "not-started"
start: 
end: 
objective: "AI security & supply chain: prompt injection, data exfil, dependency compromise, MCP risk, guardrails."
concepts: ["[[AI Gateway]]", "[[MCP]]"]
project: ["[[Level 7 — Production-grade AI platform]]"]
deliverable: 
tags: ["week", "phase/6"]
---

# Week 49 — AI security & supply chain

**Phase:** [[Phase 6 — Reliability, Agents, Scale Simulation & Your Specialization]]  
**Objective:** AI security & supply chain: prompt injection, data exfil, dependency compromise, MCP risk, guardrails.  
**Concepts:** [[AI Gateway]], [[MCP]]
**Project:** [[Level 7 — Production-grade AI platform]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
OWASP LLM Top 10; a 2026 AI-supply-chain incident writeup.

1. Read the OWASP LLM Top 10.
2. Learn injection, data exfil, supply-chain risk, and guardrails.
3. Write your guardrail placement (input vs output).

## Read (15m)
A red-team / AI-security engineering post.

1. Read a 2026 AI-supply-chain incident writeup + a red-team post.
2. Note the indirect-injection vector (via retrieved/tool content).
3. Write your largest attack surface.

## Build (20m)
Add semantic guardrails (prompt-injection/PII scanners) at your gateway; pin and verify your AI dependency supply chain.

## Step-by-step
1. Add semantic guardrails at your gateway: prompt-injection and PII scanners on input/output.
2. Pin and verify your AI dependency supply chain (model hashes, MCP servers, packages).
3. Run the OWASP LLM Top-10 scenarios against your stack and log what gets through.
4. Map your largest attack surface: model, tools (MCP), data, or dependencies.

## Reflect (5m)
> What's your largest attack surface — the model, the tools (MCP), the data, or the dependencies?

## Done when
- [ ] Guardrails (injection/PII) active at the gateway.
- [ ] A pinned, verified dependency supply chain.
- [ ] A ranked attack-surface assessment for your platform.

## Common pitfalls
- Guardrails add latency and false positives — measure and tune, don't bolt on blindly.
- Indirect injection (via retrieved docs/tool output) bypasses input-only filters.

## Resources
- [[OWASP LLM Top 10]]
- [[Import AI]]

## Go deeper
- OWASP LLM Top 10.
- A 2026 AI-supply-chain incident writeup; a red-team engineering post.

## Tasks
- [ ] Study/open [[OWASP LLM Top 10]]
- [ ] Study/open [[Import AI]]
- [ ] **Build:** Add semantic guardrails (prompt-injection/PII scanners) at your gateway; pin and verify your AI dependency supply chain.
- [ ] Guardrails (injection/PII) active at the gateway.
- [ ] A pinned, verified dependency supply chain.
- [ ] A ranked attack-surface assessment for your platform.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
