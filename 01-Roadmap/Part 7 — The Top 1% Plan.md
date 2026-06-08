---
type: "roadmap-part"
part: 7
tags: ["roadmap", "part/7"]
---

# Part 7 — The Top 1% Plan

*If becoming one of the world's best AI infra engineers in 24 months (full-time job, 1 hour/day) were the only goal.*

## What I would learn (priority order)
1. **The [[KV Cache]] and the prefill/decode split**, until second nature — highest leverage in the field.
2. **GPU scheduling on Kubernetes** ([[DRA]] + an AI-aware scheduler) — the rarest hands-on platform skill.
3. **[[Collective Communication (NCCL)]] + high-performance networking** (RDMA, NVLink/IB topology) — rarest, best-paid, most durable.
4. **Disaggregated/distributed serving** ([[Disaggregated Serving]], Dynamo/llm-d) end-to-end.
5. **Distributed training enough to be dangerous** (parallelism, [[ZeRO and FSDP]], checkpointing, fault tolerance).
6. **[[AI Reliability Engineering]]** — your SRE background's killer app.
7. **[[AI Cost Engineering]]** — always relevant, compounds forever.

## What I would deliberately ignore
Becoming an ML researcher (no backprop, no novel architectures) · RLHF/DPO/fine-tuning internals · writing CUDA kernels (initially) · naive RAG & prompt-engineering content · chasing every new framework · tool zoos / agent-framework churn.

## Mandatory papers (architecture + results, skip the proofs)
[[Attention Is All You Need]], [[PagedAttention (vLLM)]], [[RadixAttention (SGLang)]], [[Megatron-LM]], [[ZeRO (DeepSpeed)]], [[PyTorch FSDP]], [[DistServe & Splitwise]], [[FlashAttention (1 & 2)]], [[Switch Transformer & GShard (MoE)]], [[Speculative Decoding]], [[Llama, DeepSeek & Qwen Technical Reports]]

## Skills that create the biggest leverage (ranked)
1. Debugging distributed GPU systems under failure ([[Stragglers and SDC]]). 2. GPU scheduling/multi-tenancy on K8s. 3. AI networking depth. 4. Disaggregated serving design & tuning. 5. Cost engineering at fleet scale. 6. Reliability discipline applied to AI.

## The single most important habit
**Build and publish in public, every week.** The 5-minute daily Reflect compounds into a learning log; each phase deliverable becomes a public artifact. The top 1% built the rare thing and showed their work.


---
*Source: `ai-infra-roadmap.md`. This note is a faithful summary; the roadmap is the source of truth.*
