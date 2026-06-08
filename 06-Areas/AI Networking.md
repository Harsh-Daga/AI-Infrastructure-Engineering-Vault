---
type: "area"
ranked: "yes"
demand: 4
comp: 5
depth: 5
difficulty: 5
longevity: 5
tags: ["area", "area/ai-networking"]
---

# AI Networking

> Collective comms, lossless fabrics (IB/RoCE), NVLink topology, RDMA.

## Part 1 ranking (1–5)
| Demand | Comp | Depth | Difficulty | Longevity |
|---|---|---|---|---|
| 4 | 5 | 5 | 5 | 5 |

## Concepts in this area

- [[Cluster Topology]]
- [[Collective Communication (NCCL)]]
- [[GPU Memory Hierarchy]]
- [[InfiniBand vs RoCE]]
- [[NVLink and NVSwitch]]
- [[RDMA]]

## Weeks that cover it

- [[Week 05 — GPU architecture & memory hierarchy]]
- [[Week 16 — Multi-GPU single-node serving]]
- [[Week 33 — Collective communication & NCCL]]
- [[Week 34 — RDMA, InfiniBand, RoCEv2 & lossless fabrics]]
- [[Week 35 — Cluster topology — NVLink, NVSwitch, rails]]

## Projects

- [[Level 8 — Frontier-scale architecture simulation]]

## Resources

- [[Computer Architecture — A Quantitative Approach]]
- [[Hugging Face Ultra-Scale Playbook]]
- [[NVIDIA Deep Learning Institute (DLI)]]
- [[NVIDIA Technical Blog]]
- [[Meta Engineering & PyTorch Blog]]
- [[Cloudflare Blog]]
- [[Switch Transformer & GShard (MoE)]]
- [[nccl]]
- [[nccl-tests]]
- [[SemiAnalysis]]
- [[NVIDIA Developer + GTC Recordings]]

## Live view (DataviewJS)
<!-- Requires the Dataview plugin. Lists every note tagged to this area automatically. -->
```dataviewjs
const slug = "area/ai-networking";
const pages = dv.pages("#" + slug).sort(p => p.type);
dv.table(["Note", "Type", "Difficulty", "Status/Mastery"],
  pages.map(p => [p.file.link, p.type, p.difficulty ?? "",
    p.status ?? (p.mastery !== undefined ? "mastery " + p.mastery : "")]));
```
