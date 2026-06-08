---
type: "concept"
area: "[[AI Networking]]"
difficulty: 5
mastery: 0
prerequisites: ["[[RDMA]]"]
unlocks: ["[[Cluster Topology]]"]
tags: ["concept", "area/ai-networking"]
---

# InfiniBand vs RoCE

Two ways to run RDMA at datacenter scale: InfiniBand (purpose-built lossless fabric) vs RoCEv2 (RDMA over Ethernet, made lossless with PFC/ECN and careful congestion control). The choice drives cost, operational complexity, and how far you scale.

> [!info] Why it matters for an infra engineer
> The fabric, not the GPU, often decides how large a run can scale. Knowing IB vs RoCE tradeoffs is core AI-networking depth.

## Related

- **Area:** [[AI Networking]]
- **Prerequisites:** [[RDMA]]
- **Unlocks:** [[Cluster Topology]]
- **Studied in:** [[Week 34 — RDMA, InfiniBand, RoCEv2 & lossless fabrics]]
- **Resources:** [[Meta Engineering & PyTorch Blog]], [[SemiAnalysis]]

## Notes
