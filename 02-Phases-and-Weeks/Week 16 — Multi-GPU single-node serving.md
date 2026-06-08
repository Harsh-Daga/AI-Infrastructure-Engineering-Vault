---
type: "week"
week: 16
phase: "Phase 2 — LLM Serving, Deep"
status: "not-started"
start: 
end: 
objective: "Multi-GPU single-node serving (tensor parallelism): NVLink intra-node comms."
concepts: ["[[Tensor Parallelism]]", "[[NVLink and NVSwitch]]", "[[Collective Communication (NCCL)]]"]
project: []
deliverable: "Phase-2 deliverable: a benchmarked comparison report (vLLM vs SGLang vs TRT-LLM on your workload) with a decision matrix."
tags: ["week", "phase/2"]
---

# Week 16 — Multi-GPU single-node serving

**Phase:** [[Phase 2 — LLM Serving, Deep]]  
**Objective:** Multi-GPU single-node serving (tensor parallelism): NVLink intra-node comms.  
**Concepts:** [[Tensor Parallelism]], [[NVLink and NVSwitch]], [[Collective Communication (NCCL)]]

## Learn (20m)
vLLM/TensorRT-LLM tensor-parallel docs; an intro to NCCL collectives (preview of Phase 5).

## Read (15m)
A writeup on TP vs PP for inference.

## Build (20m)
If you have multi-GPU access (or rent a 2×/4× node hourly), serve a model with `tensor-parallel-size > 1`; measure scaling efficiency.

## Reflect (5m)
> Why is intra-node NVLink bandwidth the thing that makes (or breaks) tensor-parallel serving?

## Resources
- [[vLLM Documentation]]
- [[nccl]]
- [[NVIDIA Deep Learning Institute (DLI)]]

## Tasks
- [ ] Study/open [[vLLM Documentation]]
- [ ] Study/open [[nccl]]
- [ ] Study/open [[NVIDIA Deep Learning Institute (DLI)]]
- [ ] **Build:** If you have multi-GPU access (or rent a 2×/4× node hourly), serve a model with `tensor-parallel-size > 1`; measure scaling efficiency.
- [ ] **Reflect:** answer the week's question in the learning log

## Phase deliverable
> [!success] Phase-2 deliverable: a benchmarked comparison report (vLLM vs SGLang vs TRT-LLM on your workload) with a decision matrix.

## Notes
