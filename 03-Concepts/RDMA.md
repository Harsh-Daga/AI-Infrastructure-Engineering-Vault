---
type: "concept"
area: "[[AI Networking]]"
difficulty: 5
mastery: 0
prerequisites: []
unlocks: ["[[Disaggregated Serving]]", "[[InfiniBand vs RoCE]]"]
tags: ["concept", "area/ai-networking"]
---

# RDMA

Remote Direct Memory Access: zero-copy, kernel-bypass data movement between nodes' memory (and GPU memory, via GPUDirect). The physical substrate of multi-GPU AI — KV transfer (NIXL), gradient sync, checkpoint I/O all ride on it. Verbs, queue pairs, lossless delivery.

> [!info] Why it matters for an infra engineer
> RDMA is one of the rarest and best-paid sub-skills in the field. It's what makes disaggregation and large-scale training physically possible.

## Related

- **Area:** [[AI Networking]]
- **Unlocks:** [[Disaggregated Serving]], [[InfiniBand vs RoCE]]
- **Studied in:** [[Week 34 — RDMA, InfiniBand, RoCEv2 & lossless fabrics]]
- **Resources:** [[NVIDIA Deep Learning Institute (DLI)]], [[Meta Engineering & PyTorch Blog]]

## Notes
