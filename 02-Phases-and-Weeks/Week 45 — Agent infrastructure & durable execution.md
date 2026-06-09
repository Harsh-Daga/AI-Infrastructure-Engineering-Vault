---
type: "week"
week: 45
phase: "Phase 6 — Reliability, Agents, Scale Simulation & Your Specialization"
status: "not-started"
start: 
end: 
objective: "Agent infrastructure & durable execution: multi-step agents, Temporal/Restate, retries/idempotency."
concepts: ["[[Durable Execution]]"]
project: ["[[Level 7 — Production-grade AI platform]]"]
deliverable: 
tags: ["week", "phase/6"]
---

# Week 45 — Agent infrastructure & durable execution

**Phase:** [[Phase 6 — Reliability, Agents, Scale Simulation & Your Specialization]]  
**Objective:** Agent infrastructure & durable execution: multi-step agents, Temporal/Restate, retries/idempotency.  
**Concepts:** [[Durable Execution]]
**Project:** [[Level 7 — Production-grade AI platform]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
Temporal/Restate docs; an "agents need durable execution" talk.

## Read (15m)
A production agent-infra engineering post.

## Build (20m)
Build a durable multi-step agent (e.g. with Temporal) that survives a worker crash mid-task and resumes.

## Step-by-step
1. Model a multi-step agent task as a durable workflow (Temporal or Restate).
2. Make each tool call an activity with retries and idempotency keys.
3. Run the workflow, kill the worker mid-task, and confirm it resumes from the last step.
4. Verify no double-execution of side effects after the crash.

## Reflect (5m)
> Why are agents a workflow-orchestration problem more than a model problem?

## Done when
- [ ] A durable agent that survives a worker crash and resumes.
- [ ] Idempotent activities that don't double-execute side effects.
- [ ] You can explain why agents are an orchestration problem more than a model problem.

## Common pitfalls
- Non-idempotent tool calls (charges, sends) get re-run on retry without idempotency keys.
- Putting LLM calls in the workflow path (not activities) breaks determinism on replay.

## Resources
- [[temporal]]
- [[restate]]
- [[Anthropic Engineering]]

## Go deeper
- Temporal / Restate docs.
- An "agents need durable execution" talk + a production agent-infra post.

## Tasks
- [ ] Study/open [[temporal]]
- [ ] Study/open [[restate]]
- [ ] Study/open [[Anthropic Engineering]]
- [ ] **Build:** Build a durable multi-step agent (e.g. with Temporal) that survives a worker crash mid-task and resumes.
- [ ] A durable agent that survives a worker crash and resumes.
- [ ] Idempotent activities that don't double-execute side effects.
- [ ] You can explain why agents are an orchestration problem more than a model problem.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
