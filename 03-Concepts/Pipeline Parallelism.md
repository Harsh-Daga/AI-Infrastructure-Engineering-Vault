---
type: "concept"
area: "[[Distributed Training]]"
difficulty: 4
mastery: 0
prerequisites: ["[[Collective Communication (NCCL)]]"]
unlocks: []
tags: ["concept", "area/distributed-training"]
---

# Pipeline Parallelism

Split the model by *layers* into stages across GPUs/nodes, streaming micro-batches through to hide the inter-stage bubble. Cheaper on bandwidth than TP, so it spans nodes — but the bubble and load-balance are the tuning challenge.

> [!info] Why it matters for an infra engineer
> PP is how you go cross-node when TP runs out of NVLink. Knowing TP-vs-PP tradeoffs is core to placing big jobs.

## Related

- **Area:** [[Distributed Training]]
- **Prerequisites:** [[Collective Communication (NCCL)]]
- **Studied in:** [[Week 37 — Parallelism taxonomy for training]]
- **Resources:** [[Megatron-LM]], [[Hugging Face Ultra-Scale Playbook]]

## Notes
