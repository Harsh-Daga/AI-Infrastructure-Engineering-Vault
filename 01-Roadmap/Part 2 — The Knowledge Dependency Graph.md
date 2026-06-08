---
type: "roadmap-part"
part: 2
tags: ["roadmap", "part/2"]
---

# Part 2 — The Knowledge Dependency Graph

The whole vault's graph view *is* this dependency DAG. Every concept note declares `prerequisites:` and `unlocks:`; open the graph and filter to `#concept` to see the backbone.

## The core dependency chain
You already have **Linux · Cloud · K8s · IaC · Networking · Observability · Ops**. On top of that:

- **AI foundations (just enough):** [[Tokenization]] → [[Embeddings]] → [[Attention]] → [[Transformer Block]] → **[[KV Cache]] ★** → [[Quantization]] · [[Mixture of Experts]] · [[Reasoning Models]]
- **Infra foundations (deep):** CPU arch / NUMA / cache → [[GPU Memory Hierarchy]] → storage → networking internals → **[[RDMA]] · [[InfiniBand vs RoCE]] · [[NVLink and NVSwitch]] ★**
- **Distributed systems (sharpen):** [[CAP]] · [[Consistency Models]] · [[Raft]] · [[Queueing and Backpressure]]
- **GPU systems (the bridge):** [[GPU Memory Hierarchy]] · [[GPU Profiling]] · **[[Collective Communication (NCCL)]] ★** · the serving fundamentals ([[Continuous Batching]] · [[PagedAttention]] · [[RadixAttention and Prefix Caching]] · [[Speculative Decoding]] · [[TTFT vs ITL]])
- **Then it forks:** [[Distributed Training]] (parallelism, [[ZeRO and FSDP]], checkpointing) and [[Inference Infrastructure]] ([[KV Routing]], [[Disaggregated Serving]], gateways, autoscaling, cost)
- **Converging on:** AI Platform + Reliability Engineering (scheduling via [[DRA]]/KAI, SLOs, fault tolerance, agents, the paved road) — the staff-level destination.

## The two highest-leverage low-level concepts
★ **[[KV Cache]]** ties together attention, memory, and inference. ★ **[[Collective Communication (NCCL)]] + high-performance networking** ties together RDMA, NVLink, and distributed training + inference.

## What to skip initially
Paxos in depth · RLHF/DPO internals · CUDA kernel authoring · attention gradient math · building a vector index from scratch. (See [[Part 7 — The Top 1% Plan]] in Part 7.)


---
*Source: `ai-infra-roadmap.md`. This note is a faithful summary; the roadmap is the source of truth.*
