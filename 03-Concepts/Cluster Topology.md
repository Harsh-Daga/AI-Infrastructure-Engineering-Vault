---
type: "concept"
area: "[[AI Networking]]"
difficulty: 5
mastery: 0
prerequisites: ["[[NVLink and NVSwitch]]", "[[InfiniBand vs RoCE]]", "[[Collective Communication (NCCL)]]"]
unlocks: []
tags: ["concept", "area/ai-networking"]
---

# Cluster Topology

How GPUs, NVSwitch domains, and leaf/spine fabric compose into a cluster — and why **rail-optimized** topologies and topology-aware placement minimize cross-rail collective traffic. You place an 8-way TP + 4-way PP job to keep the heaviest collectives on the fastest links.

> [!info] Why it matters for an infra engineer
> Topology-aware placement is a scheduling superpower. The same job can be fast or fabric-bound depending on where you put it.

## Related

- **Area:** [[AI Networking]]
- **Prerequisites:** [[NVLink and NVSwitch]], [[InfiniBand vs RoCE]], [[Collective Communication (NCCL)]]
- **Studied in:** [[Week 35 — Cluster topology — NVLink, NVSwitch, rails]]
- **Resources:** [[NVIDIA Technical Blog]], [[Hugging Face Ultra-Scale Playbook]]
- **Projects:** [[Level 8 — Frontier-scale architecture simulation]]

## Notes
