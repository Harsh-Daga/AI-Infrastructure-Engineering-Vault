---
type: "week"
week: 44
phase: "Phase 6 — Reliability, Agents, Scale Simulation & Your Specialization"
status: "not-started"
start: 
end: 
objective: "Failure injection & chaos for AI systems: dependency failure, load-shedding, fallback routing."
concepts: ["[[AI Reliability Engineering]]", "[[Queueing and Backpressure]]"]
project: ["[[Level 7 — Production-grade AI platform]]"]
deliverable: 
tags: ["week", "phase/6"]
---

# Week 44 — Failure injection & chaos for AI

**Phase:** [[Phase 6 — Reliability, Agents, Scale Simulation & Your Specialization]]  
**Objective:** Failure injection & chaos for AI systems: dependency failure, load-shedding, fallback routing.  
**Concepts:** [[AI Reliability Engineering]], [[Queueing and Backpressure]]
**Project:** [[Level 7 — Production-grade AI platform]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
Chaos-engineering principles; load-shedding patterns.

1. Read chaos-engineering principles.
2. Learn load-shedding and fallback-routing patterns.
3. Write your degradation ladder.

## Read (15m)
A resilience-pattern writeup applied to LLM systems.

1. Read a resilience-pattern writeup applied to LLM systems.
2. Note their retry/backoff strategy.
3. Write how they avoid retry storms.

## Build (20m)
Inject failures (kill a decode worker, throttle the fabric, fail a provider); verify graceful degradation and recovery.

## Step-by-step
1. Define a degradation ladder: big model → small model → cached/templated response → graceful error.
2. Inject failures: kill a decode worker, throttle the fabric, fail a provider.
3. Verify load-shedding and fallback routing kick in and recover.
4. Confirm quality degrades gracefully (not a cliff) at each rung.

## Reflect (5m)
> When the big model is down, what's your degradation ladder — and does quality degrade gracefully or cliff?

## Done when
- [ ] Observed graceful degradation and recovery under injected failures.
- [ ] A written degradation ladder for "big model down."
- [ ] Evidence that quality degrades smoothly, not catastrophically.

## Common pitfalls
- Retries without backoff/jitter turn a blip into a self-inflicted outage.
- Fallbacks that are never exercised rot — test them in chaos drills, not in prod incidents.

## Resources
- [[Google SRE Book & Workbook]]
- [[Uber, Netflix & Stripe Engineering]]

## Go deeper
- Chaos-engineering principles; load-shedding patterns.
- A resilience-pattern writeup applied to LLM systems.

## Tasks
- [ ] Study/open [[Google SRE Book & Workbook]]
- [ ] Study/open [[Uber, Netflix & Stripe Engineering]]
- [ ] **Build:** Inject failures (kill a decode worker, throttle the fabric, fail a provider); verify graceful degradation and recovery.
- [ ] Observed graceful degradation and recovery under injected failures.
- [ ] A written degradation ladder for "big model down."
- [ ] Evidence that quality degrades smoothly, not catastrophically.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
