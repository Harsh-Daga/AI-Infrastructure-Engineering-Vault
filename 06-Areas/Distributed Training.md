---
type: "area"
ranked: "yes"
demand: 4
comp: 5
depth: 5
difficulty: 5
longevity: 4
tags: ["area", "area/distributed-training"]
---

# Distributed Training

> 3D/5D parallelism, checkpointing, recovery at scale.

## Part 1 ranking (1–5)
| Demand | Comp | Depth | Difficulty | Longevity |
|---|---|---|---|---|
| 4 | 5 | 5 | 5 | 4 |

## Concepts in this area

- [[Context Parallelism]]
- [[Data Parallelism]]
- [[Expert Parallelism]]
- [[Mixture of Experts]]
- [[Pipeline Parallelism]]
- [[Tensor Parallelism]]
- [[ZeRO and FSDP]]

## Weeks that cover it

- [[Week 08 — Model families & what they cost to run]]
- [[Week 16 — Multi-GPU single-node serving]]
- [[Week 37 — Parallelism taxonomy for training]]
- [[Week 38 — Training frameworks — Megatron, FSDP2, DeepSpeed]]

## Resources

- [[Designing Data-Intensive Applications]]
- [[Programming Massively Parallel Processors]]
- [[Hugging Face Ultra-Scale Playbook]]
- [[Meta Engineering & PyTorch Blog]]
- [[Databricks (Mosaic) Engineering]]
- [[Hugging Face Blog]]
- [[Megatron-LM]]
- [[ZeRO (DeepSpeed)]]
- [[PyTorch FSDP]]
- [[Switch Transformer & GShard (MoE)]]
- [[Llama, DeepSeek & Qwen Technical Reports]]
- [[Megatron-LM]]
- [[torchtitan]]
- [[DeepSpeed]]
- [[nanotron]]

## Live view (DataviewJS)
<!-- Requires the Dataview plugin. Lists every note tagged to this area automatically. -->
```dataviewjs
const slug = "area/distributed-training";
const pages = dv.pages("#" + slug).sort(p => p.type);
dv.table(["Note", "Type", "Difficulty", "Status/Mastery"],
  pages.map(p => [p.file.link, p.type, p.difficulty ?? "",
    p.status ?? (p.mastery !== undefined ? "mastery " + p.mastery : "")]));
```
