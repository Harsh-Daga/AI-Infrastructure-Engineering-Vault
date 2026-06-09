---
type: "week"
week: 5
phase: "Phase 1 — Foundations"
status: "not-started"
start: 
end: 
objective: "GPU architecture & memory hierarchy: SMs, HBM bandwidth, compute-bound vs memory-bound."
concepts: ["[[GPU Memory Hierarchy]]"]
project: ["[[Level 1 — Run local LLMs]]"]
deliverable: 
tags: ["week", "phase/1"]
---

# Week 05 — GPU architecture & memory hierarchy

**Phase:** [[Phase 1 — Foundations]]  
**Objective:** GPU architecture & memory hierarchy: SMs, HBM bandwidth, compute-bound vs memory-bound.  
**Concepts:** [[GPU Memory Hierarchy]]
**Project:** [[Level 1 — Run local LLMs]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
NVIDIA "GPU architecture" overview; Horace He "Making Deep Learning Go Brrrr From First Principles."

1. Read the NVIDIA GPU-architecture overview: SMs, warps, HBM, the memory hierarchy.
2. Watch/read Horace He's "Brrrr" for compute-bound vs memory-bound thinking.
3. Write the roofline idea in one sentence (arithmetic intensity vs the ridge point).

## Read (15m)
A datacenter GPU spec sheet (H100/H200/B200) — read FLOPs, HBM bandwidth, NVLink BW as the numbers that bound your system.

1. Open an H100/H200/B200 spec sheet.
2. Copy down peak FLOPs, HBM bandwidth, and NVLink bandwidth.
3. Note which of these bounds LLM decode (hint: bandwidth).

## Build (20m)
Run `nvidia-smi`, `nvidia-smi dmon`, `nvtop`; saturate a GPU and watch utilization, memory, power, clocks.

## Step-by-step
1. Read your GPU's spec sheet; write down peak FLOPs, HBM bandwidth, and NVLink BW.
2. Run `nvidia-smi dmon` / `nvtop` while running a compute-heavy and a memory-heavy kernel.
3. Compute arithmetic intensity (FLOPs/byte) for a matmul vs an elementwise op; place each on the roofline.
4. Identify whether decode (small matmuls, big weight reads) is compute- or memory-bound — and why.

## Reflect (5m)
> Map CPU concepts you know (cache, NUMA, bandwidth) onto the GPU. Where do the analogies break?

## Done when
- [ ] You can place LLM decode on the roofline and justify it as memory-bound.
- [ ] You watched utilization, memory, power, and clocks change with workload.
- [ ] You mapped CPU cache/NUMA/bandwidth concepts onto the GPU.

## Common pitfalls
- "GPU-util 100%" in nvidia-smi means a kernel is resident, not that math units are busy.
- Thermal/power throttling silently lowers clocks — watch the clock column.

## Resources
- [[Horace He — Making Deep Learning Go Brrrr]]
- [[Programming Massively Parallel Processors]]
- [[Horace He & PyTorch Talks]]

## Go deeper
- Horace He, "Making Deep Learning Go Brrrr From First Principles."
- NVIDIA H100/H200/B200 architecture whitepaper — the numbers that bound your system.

## Tasks
- [ ] Study/open [[Horace He — Making Deep Learning Go Brrrr]]
- [ ] Study/open [[Programming Massively Parallel Processors]]
- [ ] Study/open [[Horace He & PyTorch Talks]]
- [ ] **Build:** Run `nvidia-smi`, `nvidia-smi dmon`, `nvtop`; saturate a GPU and watch utilization, memory, power, clocks.
- [ ] You can place LLM decode on the roofline and justify it as memory-bound.
- [ ] You watched utilization, memory, power, and clocks change with workload.
- [ ] You mapped CPU cache/NUMA/bandwidth concepts onto the GPU.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
