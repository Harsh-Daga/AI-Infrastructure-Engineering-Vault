---
type: "week"
week: 36
phase: "Phase 5 — Networking, Distributed Systems for AI, Distributed Training"
status: "not-started"
start: 
end: 
objective: "Distributed systems for AI: coordination, discovery, consistency, queueing/backpressure."
concepts: ["[[CAP]]", "[[Consistency Models]]", "[[Raft]]", "[[Queueing and Backpressure]]"]
project: []
deliverable: 
tags: ["week", "phase/5"]
---

# Week 36 — Distributed systems for AI — coordination

**Phase:** [[Phase 5 — Networking, Distributed Systems for AI, Distributed Training]]  
**Objective:** Distributed systems for AI: coordination, discovery, consistency, queueing/backpressure.  
**Concepts:** [[CAP]], [[Consistency Models]], [[Raft]], [[Queueing and Backpressure]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
Re-read the relevant chapters of Designing Data-Intensive Applications (replication, consistency, consensus) with an AI lens.

1. Re-read DDIA chapters (replication, consistency, consensus) with an AI lens.
2. Map each to inference coordination (discovery, registration, backpressure).
3. Write the consistency model your discovery layer needs.

## Read (15m)
A distributed-inference coordination design doc (Dynamo discovery / llm-d).

1. Read a Dynamo/llm-d coordination design doc.
2. Note their discovery + health-check design.
3. Write which classic failure mode it guards against.

## Build (20m)
Add health-checked worker registration + discovery to your disaggregated setup; kill a worker and observe recovery.

## Step-by-step
1. Re-read DDIA chapters on replication, consistency, and consensus with an inference lens.
2. Add health-checked worker registration + service discovery to your disaggregated setup.
3. Kill a worker mid-traffic; observe detection time and recovery (re-routing).
4. Introduce a stale-discovery or thundering-herd scenario and see how the system copes.

## Reflect (5m)
> Which classic distributed-systems failure modes (split brain, stale discovery, thundering herd) show up in disaggregated serving?

## Done when
- [ ] Workers self-register and are discovered; a killed worker is detected and routed around.
- [ ] You reproduced at least one classic failure mode (split-brain/stale discovery/thundering herd).
- [ ] You can map distributed-systems failures onto disaggregated serving.

## Common pitfalls
- Health checks that are too lax keep routing to dead workers; too aggressive flap under load.
- On recovery, a thundering herd of retries can take down the recovered worker again.

## Resources
- [[Designing Data-Intensive Applications]]
- [[MIT 6.824 Distributed Systems]]
- [[NVIDIA Dynamo Documentation]]

## Go deeper
- Designing Data-Intensive Applications (replication/consistency/consensus).
- A Dynamo/llm-d discovery design doc; MIT 6.824 lectures.

## Tasks
- [ ] Study/open [[Designing Data-Intensive Applications]]
- [ ] Study/open [[MIT 6.824 Distributed Systems]]
- [ ] Study/open [[NVIDIA Dynamo Documentation]]
- [ ] **Build:** Add health-checked worker registration + discovery to your disaggregated setup; kill a worker and observe recovery.
- [ ] Workers self-register and are discovered; a killed worker is detected and routed around.
- [ ] You reproduced at least one classic failure mode (split-brain/stale discovery/thundering herd).
- [ ] You can map distributed-systems failures onto disaggregated serving.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
