---
type: "week"
week: 50
phase: "Phase 6 — Reliability, Agents, Scale Simulation & Your Specialization"
status: "not-started"
start: 
end: 
objective: "Frontier-scale architecture simulation (paper exercise): a 10k–100k GPU fleet on paper."
concepts: ["[[Cluster Topology]]", "[[InfiniBand vs RoCE]]", "[[ZeRO and FSDP]]", "[[Checkpointing and Fault Tolerance]]", "[[AI Cost Engineering]]"]
project: ["[[Level 8 — Frontier-scale architecture simulation]]"]
deliverable: 
tags: ["week", "phase/6"]
---

# Week 50 — Frontier-scale architecture simulation

**Phase:** [[Phase 6 — Reliability, Agents, Scale Simulation & Your Specialization]]  
**Objective:** Frontier-scale architecture simulation (paper exercise): a 10k–100k GPU fleet on paper.  
**Concepts:** [[Cluster Topology]], [[InfiniBand vs RoCE]], [[ZeRO and FSDP]], [[Checkpointing and Fault Tolerance]], [[AI Cost Engineering]]
**Project:** [[Level 8 — Frontier-scale architecture simulation]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
Re-read the Ultra-Scale Playbook + frontier-lab infra writeups with design intent.

1. Re-read the Ultra-Scale Playbook + frontier-lab writeups with design intent.
2. Study a reference hyperscale architecture.
3. Write the three things that break first at 100k GPUs.

## Read (15m)
Public descriptions of hyperscale AI clusters (Meta, NVIDIA reference architectures).

1. Read public hyperscale cluster descriptions (Meta, NVIDIA reference architectures).
2. Note their failure-handling and cost structure.
3. Write what their design optimizes for.

## Build (20m)
Write a full architecture doc: topology, scheduler, serving stack, observability, failure handling, and a cost model for a frontier-scale fleet.

## Step-by-step
1. Re-read the Ultra-Scale Playbook + frontier-lab infra writeups with design intent.
2. Write a full architecture doc for a 10k–100k GPU fleet: topology, scheduler, serving stack.
3. Add observability, failure handling, and a cost model to the doc.
4. Identify the three things that break first at 100k GPUs and how your design handles them.

## Reflect (5m)
> What are the three things that break first at 100k GPUs, and how does your design handle them?

## Done when
- [ ] A complete frontier-scale architecture doc (topology→serving→observability→cost).
- [ ] A named top-3 failure list at 100k GPUs with mitigations.
- [ ] A defensible cost model.

## Common pitfalls
- Designing for the happy path is the trap — at 100k GPUs something is always failing.
- Cost models that ignore network, power, and idle time are fiction.

## Resources
- [[Hugging Face Ultra-Scale Playbook]]
- [[Meta Engineering & PyTorch Blog]]
- [[NVIDIA Technical Blog]]
- [[SemiAnalysis]]

## Go deeper
- Ultra-Scale Playbook + frontier-lab infra writeups.
- Public hyperscale cluster descriptions (Meta, NVIDIA reference architectures).

## Tasks
- [ ] Study/open [[Hugging Face Ultra-Scale Playbook]]
- [ ] Study/open [[Meta Engineering & PyTorch Blog]]
- [ ] Study/open [[NVIDIA Technical Blog]]
- [ ] Study/open [[SemiAnalysis]]
- [ ] **Build:** Write a full architecture doc: topology, scheduler, serving stack, observability, failure handling, and a cost model for a frontier-scale fleet.
- [ ] A complete frontier-scale architecture doc (topology→serving→observability→cost).
- [ ] A named top-3 failure list at 100k GPUs with mitigations.
- [ ] A defensible cost model.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
