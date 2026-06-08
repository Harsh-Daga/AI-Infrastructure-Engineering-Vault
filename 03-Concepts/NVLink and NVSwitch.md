---
type: "concept"
area: "[[AI Networking]]"
difficulty: 4
mastery: 0
prerequisites: ["[[GPU Memory Hierarchy]]"]
unlocks: ["[[Cluster Topology]]", "[[Tensor Parallelism]]"]
tags: ["concept", "area/ai-networking"]
---

# NVLink and NVSwitch

High-bandwidth **intra-node** GPU interconnect (NVLink links, NVSwitch crossbar) — an order of magnitude faster than the inter-node fabric. It's what makes tensor-parallel serving viable inside a box; cross-node TP falls off a cliff.

> [!info] Why it matters for an infra engineer
> Intra-node NVLink bandwidth is the thing that makes or breaks tensor-parallel serving. Placement decisions live and die by it.

## Related

- **Area:** [[AI Networking]]
- **Prerequisites:** [[GPU Memory Hierarchy]]
- **Unlocks:** [[Cluster Topology]], [[Tensor Parallelism]]
- **Studied in:** [[Week 16 — Multi-GPU single-node serving]], [[Week 35 — Cluster topology — NVLink, NVSwitch, rails]]
- **Resources:** [[NVIDIA Technical Blog]], [[NVIDIA Developer + GTC Recordings]]

## Notes
