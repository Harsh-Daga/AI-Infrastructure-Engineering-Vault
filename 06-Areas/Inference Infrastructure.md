---
type: "area"
ranked: "yes"
demand: 5
comp: 5
depth: 5
difficulty: 4
longevity: 5
tags: ["area", "area/inference-infrastructure"]
---

# Inference Infrastructure

> The full distributed system around serving: routing, KV, disaggregation, autoscaling.

## Part 1 ranking (1–5)
| Demand | Comp | Depth | Difficulty | Longevity |
|---|---|---|---|---|
| 5 | 5 | 5 | 4 | 5 |

## Concepts in this area

- [[CAP]]
- [[Consistency Models]]
- [[Disaggregated Serving]]
- [[Inference Autoscaling]]
- [[KV Cache]]
- [[KV Offload]]
- [[KV Routing]]
- [[PagedAttention]]
- [[Prefill vs Decode]]
- [[Queueing and Backpressure]]
- [[RadixAttention and Prefix Caching]]
- [[Raft]]
- [[Reasoning Models]]

## Weeks that cover it

- [[Week 01 — How an LLM actually runs]]
- [[Week 04 — The KV cache]]
- [[Week 08 — Model families & what they cost to run]]
- [[Week 09 — Serving fundamentals — batching]]
- [[Week 10 — vLLM in depth]]
- [[Week 11 — SGLang & RadixAttention]]
- [[Week 15 — KV cache management & offloading]]
- [[Week 29 — Inference on Kubernetes — KServe & Ray]]
- [[Week 30 — Disaggregated serving — Dynamo & llm-d]]
- [[Week 36 — Distributed systems for AI — coordination]]
- [[Week 42 — Distributed inference at scale]]

## Projects

- [[Level 1 — Run local LLMs]]
- [[Level 3 — Multi-model routing gateway + cost optimization]]
- [[Level 4 — AI platform on Kubernetes]]
- [[Level 6 — Distributed inference cluster]]

## Resources

- [[Designing Data-Intensive Applications]]
- [[vLLM Documentation]]
- [[SGLang Documentation]]
- [[NVIDIA Dynamo Documentation]]
- [[vLLM Blog — PagedAttention]]
- [[NVIDIA Technical Blog]]
- [[Anthropic Engineering]]
- [[OpenAI Engineering]]
- [[vLLM Blog]]
- [[Character.AI, Cursor & Perplexity Engineering]]
- [[LMSYS]]
- [[PagedAttention (vLLM)]]
- [[RadixAttention (SGLang)]]
- [[DistServe & Splitwise]]
- [[Llama, DeepSeek & Qwen Technical Reports]]
- [[vllm]]
- [[sglang]]
- [[dynamo]]
- [[llm-d]]
- [[kuberay]]
- [[kserve]]
- [[MIT 6.824 Distributed Systems]]
- [[NVIDIA Developer + GTC Recordings]]

## Live view (DataviewJS)
<!-- Requires the Dataview plugin. Lists every note tagged to this area automatically. -->
```dataviewjs
const slug = "area/inference-infrastructure";
const pages = dv.pages("#" + slug).sort(p => p.type);
dv.table(["Note", "Type", "Difficulty", "Status/Mastery"],
  pages.map(p => [p.file.link, p.type, p.difficulty ?? "",
    p.status ?? (p.mastery !== undefined ? "mastery " + p.mastery : "")]));
```
