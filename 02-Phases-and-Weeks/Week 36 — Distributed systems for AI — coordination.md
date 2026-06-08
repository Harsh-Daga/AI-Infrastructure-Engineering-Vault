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

## Learn (20m)
Re-read the relevant chapters of Designing Data-Intensive Applications (replication, consistency, consensus) with an AI lens.

## Read (15m)
A distributed-inference coordination design doc (Dynamo discovery / llm-d).

## Build (20m)
Add health-checked worker registration + discovery to your disaggregated setup; kill a worker and observe recovery.

## Reflect (5m)
> Which classic distributed-systems failure modes (split brain, stale discovery, thundering herd) show up in disaggregated serving?

## Resources
- [[Designing Data-Intensive Applications]]
- [[MIT 6.824 Distributed Systems]]
- [[NVIDIA Dynamo Documentation]]

## Tasks
- [ ] Study/open [[Designing Data-Intensive Applications]]
- [ ] Study/open [[MIT 6.824 Distributed Systems]]
- [ ] Study/open [[NVIDIA Dynamo Documentation]]
- [ ] **Build:** Add health-checked worker registration + discovery to your disaggregated setup; kill a worker and observe recovery.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
