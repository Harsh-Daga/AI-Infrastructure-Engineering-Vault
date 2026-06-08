---
type: "area"
ranked: "yes"
demand: 5
comp: 4
depth: 4
difficulty: 3
longevity: 5
tags: ["area", "area/llm-serving"]
---

# LLM Serving

> Turning a model + GPU into a reliable, batched, high-throughput API.

## Part 1 ranking (1–5)
| Demand | Comp | Depth | Difficulty | Longevity |
|---|---|---|---|---|
| 5 | 4 | 4 | 3 | 5 |

## Concepts in this area

- [[Attention]]
- [[Continuous Batching]]
- [[FlashAttention]]
- [[GPU Profiling]]
- [[Speculative Decoding]]
- [[TTFT vs ITL]]
- [[Tokenization]]
- [[Transformer Block]]

## Weeks that cover it

- [[Week 01 — How an LLM actually runs]]
- [[Week 02 — Tokenization, embeddings, context windows]]
- [[Week 03 — Attention & the transformer, infra lens]]
- [[Week 07 — Where the GPU time goes — profiling]]
- [[Week 09 — Serving fundamentals — batching]]
- [[Week 13 — Speculative decoding & latency tricks]]
- [[Week 14 — Serving metrics, SLOs & load testing]]

## Projects

- [[Level 1 — Run local LLMs]]

## Resources

- [[Programming Massively Parallel Processors]]
- [[AI Engineering]]
- [[Karpathy — Neural Networks Zero to Hero]]
- [[NVIDIA Deep Learning Institute (DLI)]]
- [[Hugging Face NLP Course]]
- [[vLLM Documentation]]
- [[SGLang Documentation]]
- [[Jay Alammar — The Illustrated Transformer]]
- [[vLLM Blog — PagedAttention]]
- [[Anyscale — Continuous Batching Blog]]
- [[Horace He — Making Deep Learning Go Brrrr]]
- [[Hugging Face Blog]]
- [[Modal, Replicate, Anyscale, BentoML & W&B Blogs]]
- [[vLLM Blog]]
- [[SGLang Blog]]
- [[LMSYS]]
- [[Attention Is All You Need]]
- [[FlashAttention (1 & 2)]]
- [[Speculative Decoding]]
- [[vllm]]
- [[sglang]]
- [[TensorRT-LLM]]
- [[llama.cpp]]
- [[ollama]]
- [[Ahead of AI]]
- [[Andrej Karpathy (YouTube)]]
- [[3Blue1Brown — Neural Networks series]]
- [[Horace He & PyTorch Talks]]

## Live view (DataviewJS)
<!-- Requires the Dataview plugin. Lists every note tagged to this area automatically. -->
```dataviewjs
const slug = "area/llm-serving";
const pages = dv.pages("#" + slug).sort(p => p.type);
dv.table(["Note", "Type", "Difficulty", "Status/Mastery"],
  pages.map(p => [p.file.link, p.type, p.difficulty ?? "",
    p.status ?? (p.mastery !== undefined ? "mastery " + p.mastery : "")]));
```
