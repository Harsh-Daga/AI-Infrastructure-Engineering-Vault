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

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
vLLM/TensorRT-LLM tensor-parallel docs; an intro to NCCL collectives (preview of Phase 5).

1. Read vLLM/TRT-LLM tensor-parallel docs.
2. Skim an intro to NCCL collectives (a preview of Phase 5).
3. Write why intra-node NVLink bandwidth gates tensor-parallel serving.

## Read (15m)
A writeup on TP vs PP for inference.

1. Read a "TP vs PP for inference" writeup.
2. Note when pipeline parallelism beats tensor parallelism.
3. Write the comms pattern each one uses.

## Build (20m)
If you have multi-GPU access (or rent a 2×/4× node hourly), serve a model with `tensor-parallel-size > 1`; measure scaling efficiency.

## Step-by-step
1. Rent a 2×/4× GPU node hourly (or use one you have).
2. Serve a model with `--tensor-parallel-size 2` (then 4) in vLLM or TRT-LLM.
3. Measure throughput at TP=1, 2, 4 and compute scaling efficiency (actual vs linear).
4. Watch NVLink/PCIe bandwidth during decode; correlate scaling loss with comms.
5. Write the Phase-2 deliverable: vLLM vs SGLang vs TRT-LLM decision matrix on your workload.

## Reflect (5m)
> Why is intra-node NVLink bandwidth the thing that makes (or breaks) tensor-parallel serving?

## Done when
- [ ] You have a TP=1/2/4 scaling-efficiency table.
- [ ] You can explain why intra-node NVLink bandwidth gates tensor-parallel serving.
- [ ] Phase-2 deliverable (benchmarked comparison + decision matrix) written.

## Common pitfalls
- TP across PCIe (no NVLink) scales poorly — confirm your node's interconnect.
- Scaling is sublinear; expect comms overhead, especially at small batch sizes.

## Resources
- [[vLLM Documentation]]
- [[nccl]]
- [[NVIDIA Deep Learning Institute (DLI)]]

## Go deeper
- vLLM/TensorRT-LLM tensor-parallel docs.
- A "TP vs PP for inference" writeup.

## Tasks
- [ ] Study/open [[vLLM Documentation]]
- [ ] Study/open [[nccl]]
- [ ] Study/open [[NVIDIA Deep Learning Institute (DLI)]]
- [ ] **Build:** If you have multi-GPU access (or rent a 2×/4× node hourly), serve a model with `tensor-parallel-size > 1`; measure scaling efficiency.
- [ ] You have a TP=1/2/4 scaling-efficiency table.
- [ ] You can explain why intra-node NVLink bandwidth gates tensor-parallel serving.
- [ ] Phase-2 deliverable (benchmarked comparison + decision matrix) written.
- [ ] **Reflect:** answer the week's question in the learning log

## Phase deliverable
> [!success] Phase-2 deliverable: a benchmarked comparison report (vLLM vs SGLang vs TRT-LLM on your workload) with a decision matrix.

## Notes
