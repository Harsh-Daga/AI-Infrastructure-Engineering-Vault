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

## Learn (20m)
NVIDIA "GPU architecture" overview; Horace He "Making Deep Learning Go Brrrr From First Principles."

## Read (15m)
A datacenter GPU spec sheet (H100/H200/B200) — read FLOPs, HBM bandwidth, NVLink BW as the numbers that bound your system.

## Build (20m)
Run `nvidia-smi`, `nvidia-smi dmon`, `nvtop`; saturate a GPU and watch utilization, memory, power, clocks.

## Reflect (5m)
> Map CPU concepts you know (cache, NUMA, bandwidth) onto the GPU. Where do the analogies break?

## Resources
- [[Horace He — Making Deep Learning Go Brrrr]]
- [[Programming Massively Parallel Processors]]
- [[Horace He & PyTorch Talks]]

## Tasks
- [ ] Study/open [[Horace He — Making Deep Learning Go Brrrr]]
- [ ] Study/open [[Programming Massively Parallel Processors]]
- [ ] Study/open [[Horace He & PyTorch Talks]]
- [ ] **Build:** Run `nvidia-smi`, `nvidia-smi dmon`, `nvtop`; saturate a GPU and watch utilization, memory, power, clocks.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
