---
type: "week"
week: 12
phase: "Phase 2 — LLM Serving, Deep"
status: "not-started"
start: 
end: 
objective: "TensorRT-LLM, Triton, and NIM (the NVIDIA path): AOT compilation, peak throughput, lock-in."
concepts: ["[[Quantization]]", "[[Continuous Batching]]"]
project: []
deliverable: 
tags: ["week", "phase/2"]
---

# Week 12 — TensorRT-LLM, Triton, and NIM

**Phase:** [[Phase 2 — LLM Serving, Deep]]  
**Objective:** TensorRT-LLM, Triton, and NIM (the NVIDIA path): AOT compilation, peak throughput, lock-in.  
**Concepts:** [[Quantization]], [[Continuous Batching]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
TensorRT-LLM quickstart; NVIDIA NIM overview.

1. Work through the TensorRT-LLM quickstart reading; learn the AOT-compile model.
2. Read the NVIDIA NIM overview for the packaged path.
3. Write the tradeoff: peak throughput vs build time and lock-in.

## Read (15m)
A recent H100/Blackwell benchmark comparing vLLM vs TensorRT-LLM vs SGLang.

1. Read a recent H100/Blackwell vLLM vs TRT-LLM vs SGLang benchmark.
2. Note the throughput gap and the conditions it assumes.
3. Write when the compile cost is worth it.

## Build (20m)
Compile a model with TensorRT-LLM (accept the ~20–30 min build); benchmark against your vLLM number.

## Step-by-step
1. Follow the TensorRT-LLM quickstart; accept the ~20–30 min engine build for your model.
2. Serve the compiled engine (optionally via Triton/NIM) and run your standard benchmark.
3. Compare throughput/latency against your best vLLM number on the same hardware and workload.
4. Document the build time, any quantization used, and the lock-in (rebuild on model/version change).

## Reflect (5m)
> For a model that won't change for 6 months, is the compile + lock-in worth the throughput? Make the call explicitly.

## Done when
- [ ] You have a vLLM vs TensorRT-LLM number on identical hardware and workload.
- [ ] You documented build time and operational lock-in explicitly.
- [ ] You made an explicit keep-or-skip call for a 6-month-stable model.

## Common pitfalls
- Engine builds are hardware- and version-specific — a driver/GPU change forces a rebuild.
- Peak throughput numbers often assume a specific batch/precision; match your real workload.

## Resources
- [[TensorRT-LLM]]
- [[NVIDIA Technical Blog]]
- [[NVIDIA Deep Learning Institute (DLI)]]

## Go deeper
- NVIDIA NIM overview — the packaged, supported path.
- A recent H100/Blackwell vLLM vs TRT-LLM vs SGLang benchmark.

## Tasks
- [ ] Study/open [[TensorRT-LLM]]
- [ ] Study/open [[NVIDIA Technical Blog]]
- [ ] Study/open [[NVIDIA Deep Learning Institute (DLI)]]
- [ ] **Build:** Compile a model with TensorRT-LLM (accept the ~20–30 min build); benchmark against your vLLM number.
- [ ] You have a vLLM vs TensorRT-LLM number on identical hardware and workload.
- [ ] You documented build time and operational lock-in explicitly.
- [ ] You made an explicit keep-or-skip call for a 6-month-stable model.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
