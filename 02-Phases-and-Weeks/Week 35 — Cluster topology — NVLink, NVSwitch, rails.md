---
type: "week"
week: 35
phase: "Phase 5 — Networking, Distributed Systems for AI, Distributed Training"
status: "not-started"
start: 
end: 
objective: "Cluster topology: NVLink, NVSwitch, rails, and topology-aware placement."
concepts: ["[[Cluster Topology]]", "[[NVLink and NVSwitch]]"]
project: ["[[Level 8 — Frontier-scale architecture simulation]]"]
deliverable: 
tags: ["week", "phase/5"]
---

# Week 35 — Cluster topology — NVLink, NVSwitch, rails

**Phase:** [[Phase 5 — Networking, Distributed Systems for AI, Distributed Training]]  
**Objective:** Cluster topology: NVLink, NVSwitch, rails, and topology-aware placement.  
**Concepts:** [[Cluster Topology]], [[NVLink and NVSwitch]]
**Project:** [[Level 8 — Frontier-scale architecture simulation]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
NVIDIA DGX/NVL72 topology docs; a "GPU cluster network design" talk.

## Read (15m)
An engineering post on topology-aware job placement.

## Build (20m)
Diagram a 256-GPU cluster (nodes, NVSwitch domains, leaf/spine fabric); annotate where each collective travels.

## Step-by-step
1. Study a real topology (DGX H100 / NVL72): nodes, NVSwitch domains, leaf/spine fabric.
2. Diagram a 256-GPU cluster with the intra-node and inter-node links labeled with bandwidths.
3. Trace where each collective travels (intra-node NVLink vs inter-node fabric).
4. Place an 8-way TP + 4-way PP job on the topology to minimize cross-rail traffic.

## Reflect (5m)
> How would you place an 8-way tensor-parallel + 4-way pipeline job on this topology to minimize cross-rail traffic?

## Done when
- [ ] A 256-GPU cluster diagram with NVSwitch domains and fabric.
- [ ] Annotations of where each collective travels.
- [ ] A topology-aware placement for a TP×PP job that minimizes cross-rail traffic.

## Common pitfalls
- Keep tensor-parallel groups inside an NVLink domain; spilling TP across the slow fabric kills throughput.
- Ignoring rail alignment causes congestion hotspots even with spare aggregate bandwidth.

## Resources
- [[NVIDIA Technical Blog]]
- [[NVIDIA Developer + GTC Recordings]]
- [[Hugging Face Ultra-Scale Playbook]]

## Go deeper
- NVIDIA DGX / NVL72 topology docs.
- An engineering post on topology-aware job placement.

## Tasks
- [ ] Study/open [[NVIDIA Technical Blog]]
- [ ] Study/open [[NVIDIA Developer + GTC Recordings]]
- [ ] Study/open [[Hugging Face Ultra-Scale Playbook]]
- [ ] **Build:** Diagram a 256-GPU cluster (nodes, NVSwitch domains, leaf/spine fabric); annotate where each collective travels.
- [ ] A 256-GPU cluster diagram with NVSwitch domains and fabric.
- [ ] Annotations of where each collective travels.
- [ ] A topology-aware placement for a TP×PP job that minimizes cross-rail traffic.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
