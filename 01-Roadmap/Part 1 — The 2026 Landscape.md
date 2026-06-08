---
type: "roadmap-part"
part: 1
tags: ["roadmap", "part/1"]
---

# Part 1 — The 2026 Landscape

## One-paragraph situation report
The center of gravity has shifted from **training** to **inference at scale**, and inference itself fractured into a distributed-systems problem. The biggest architectural change of 2026 is **[[Disaggregated Serving]]** — physically separating compute-bound *prefill* from memory-bound *decode* onto different GPU pools, connected by RDMA KV-cache transport. NVIDIA shipped **Dynamo 1.0 (GA, March 2026)**; the open-source **llm-d** community builds the Kubernetes-native version. GPU scheduling grew up: **[[DRA]] went GA in Kubernetes 1.34**, NVIDIA donated its DRA driver to the CNCF, and **KAI Scheduler** became the reference. Agents dragged **[[MCP]]** (now Linux Foundation) into a universal tool-connectivity standard. The serving-engine war settled into vLLM / SGLang / TensorRT-LLM. A new discipline — **[[AI Reliability Engineering]]** — is forming around the fact that GPUs fail constantly.

## The macro shifts
1. **Disaggregation is the new default mental model** — split phases, scale each independently. This is a distributed-systems job, exactly your background.
2. **The KV cache became the central data structure** — PagedAttention, RadixAttention, KV-aware routing, KV offload, zero-copy GPU-to-GPU transport (NIXL).
3. **Kubernetes won the AI control plane** — DRA replaces the integer device-plugin model; KAI/Kueue/Volcano, KubeRay, KServe; MIG/MPS for sharing.
4. **Multi-model is the norm; the AI gateway is the new edge** — LiteLLM/Portkey/Kong/Envoy AI Gateway handle keys, budgets, failover, guardrails.
5. **Observability is standardizing on OpenTelemetry GenAI conventions** (`gen_ai.*`).
6. **Agents are infrastructure** — durable execution, memory, MCP servers, per-step observability.

## Rare & highly valuable (your target zone)
Debugging NCCL/collective hangs at scale · designing disaggregated topologies & xPyD tuning · distributed training systems · GPU performance engineering · AI networking · the control plane that co-schedules training + inference · cost engineering that moves the 7–8-figure bill.

## The ranked areas
The highest-leverage quadrant (high comp + depth + longevity, reachable): **[[Inference Infrastructure]], [[AI Reliability Engineering]], [[GPU Orchestration]], [[AI Networking]], [[AI Platform Engineering]]**. See the area MOCs in `06-Areas/` for per-area rankings.


## Linked notes
[[LLM Serving]] · [[Inference Infrastructure]] · [[AI Networking]] · [[AI Observability]] · [[Agent Infrastructure]] · [[Memory Systems]] · [[Vector Databases]] · [[Retrieval Systems]] · [[AI Gateways]] · [[GPU Orchestration]] · [[AI Platform Engineering]] · [[AI Reliability Engineering]] · [[Distributed Training]] · [[Synthetic Data Pipelines]] · [[AI Security]] · [[AI Cost Optimization]] · [[AI Workload Scheduling]] · [[Multi-Model Systems]] · [[Model Routing]] · [[MCP Ecosystem]] · [[AI-Native Dev Platforms]]

---
*Source: `ai-infra-roadmap.md`. This note is a faithful summary; the roadmap is the source of truth.*
