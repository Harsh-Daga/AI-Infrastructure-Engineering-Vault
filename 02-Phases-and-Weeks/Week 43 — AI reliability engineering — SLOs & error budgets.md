---
type: "week"
week: 43
phase: "Phase 6 — Reliability, Agents, Scale Simulation & Your Specialization"
status: "not-started"
start: 
end: 
objective: "AI reliability engineering: SLOs & error budgets for model systems; what \"down\" means for an LLM."
concepts: ["[[AI Reliability Engineering]]", "[[Eval as Infrastructure]]"]
project: ["[[Level 7 — Production-grade AI platform]]"]
deliverable: 
tags: ["week", "phase/6"]
---

# Week 43 — AI reliability engineering — SLOs & error budgets

**Phase:** [[Phase 6 — Reliability, Agents, Scale Simulation & Your Specialization]]  
**Objective:** AI reliability engineering: SLOs & error budgets for model systems; what "down" means for an LLM.  
**Concepts:** [[AI Reliability Engineering]], [[Eval as Infrastructure]]
**Project:** [[Level 7 — Production-grade AI platform]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
Re-read the Google SRE book chapters on SLOs through an AI lens.

1. Re-read the Google SRE SLO chapters with an AI lens.
2. Learn error budgets and burn-rate alerts.
3. Write what "down" means for an LLM (the up-but-wrong case).

## Read (15m)
A "reliability for AI products" engineering post.

1. Read a "reliability for AI products" engineering post.
2. Note how they alert on quality, not just availability.
3. Write their error-budget policy.

## Build (20m)
Define SLOs (TTFT, availability, quality-via-eval) + error budget + alerting for your platform.

## Step-by-step
1. Re-read the Google SRE SLO chapters through an AI lens.
2. Define SLOs for your platform: TTFT, availability, and quality-via-eval.
3. Set an error budget and burn-rate alerts; decide the policy when it's exhausted.
4. Add a quality-regression alert driven by your eval harness, not just availability.

## Reflect (5m)
> How do you alert on quality regressions, not just availability?

## Done when
- [ ] Written SLOs (TTFT, availability, quality) with an error budget.
- [ ] Burn-rate alerting configured.
- [ ] You can alert on quality regressions, not just downtime.

## Common pitfalls
- For an LLM, "up but wrong" is an outage users feel — availability alone misses it.
- Error budgets without an enforcement policy are decoration; define what happens when it's spent.

## Resources
- [[Google SRE Book & Workbook]]
- [[Uber, Netflix & Stripe Engineering]]

## Go deeper
- Google SRE book — SLO and error-budget chapters.
- A "reliability for AI products" engineering post.

## Tasks
- [ ] Study/open [[Google SRE Book & Workbook]]
- [ ] Study/open [[Uber, Netflix & Stripe Engineering]]
- [ ] **Build:** Define SLOs (TTFT, availability, quality-via-eval) + error budget + alerting for your platform.
- [ ] Written SLOs (TTFT, availability, quality) with an error budget.
- [ ] Burn-rate alerting configured.
- [ ] You can alert on quality regressions, not just downtime.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
