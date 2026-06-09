---
type: "week"
week: 6
phase: "Phase 1 — Foundations"
status: "not-started"
start: 
end: 
objective: "Precision & quantization — your #1 inference lever: FP32/FP16/BF16/FP8/INT8/INT4 tradeoffs."
concepts: ["[[Quantization]]"]
project: ["[[Level 1 — Run local LLMs]]"]
deliverable: 
tags: ["week", "phase/1"]
---

# Week 06 — Precision & quantization

**Phase:** [[Phase 1 — Foundations]]  
**Objective:** Precision & quantization — your #1 inference lever: FP32/FP16/BF16/FP8/INT8/INT4 tradeoffs.  
**Concepts:** [[Quantization]]
**Project:** [[Level 1 — Run local LLMs]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
Hugging Face quantization docs/blogs; a GPTQ/AWQ explainer.

1. Read the HF quantization docs; learn the FP16/BF16/FP8/INT8/INT4 ladder.
2. Read a GPTQ/AWQ explainer for how weight quantization preserves quality.
3. Write what each precision costs in bytes per parameter.

## Read (15m)
An engineering writeup on FP8 inference results (e.g. serving-engine benchmark posts).

1. Read an FP8 inference benchmark writeup.
2. Note the reported throughput gain and any quality delta.
3. Write the one workload type where the writeup saw quality loss.

## Build (20m)
Serve the same model in FP16 vs FP8/INT4; compare VRAM, throughput, and output quality on a fixed prompt set.

## Step-by-step
1. Serve a model in FP16/BF16 and record VRAM, throughput, and outputs on a fixed 20-prompt set.
2. Serve the same model in FP8 or INT4 (AWQ/GPTQ) and repeat the exact measurements.
3. Diff the outputs prompt-by-prompt; flag any degradation in reasoning/format-sensitive prompts.
4. Tabulate VRAM saved, throughput gained, and quality delta; decide where the knee is.

## Reflect (5m)
> When is quantization free lunch, and when does it quietly cost you quality?

## Done when
- [ ] You have a side-by-side FP16 vs quantized table (VRAM, throughput, quality).
- [ ] You identified at least one prompt class where quantization hurt quality.
- [ ] You can state when quantization is free lunch vs a hidden quality tax.

## Common pitfalls
- Quality regressions hide in long-context, math, and structured-output prompts — test those.
- Different quant methods (GPTQ vs AWQ vs FP8) have different sweet spots; don't generalize from one.

## Resources
- [[Hugging Face Blog]]
- [[vLLM Blog]]

## Go deeper
- Hugging Face quantization docs/blogs (GPTQ, AWQ, bitsandbytes).
- A serving-engine FP8 benchmark post — real throughput/quality numbers.

## Tasks
- [ ] Study/open [[Hugging Face Blog]]
- [ ] Study/open [[vLLM Blog]]
- [ ] **Build:** Serve the same model in FP16 vs FP8/INT4; compare VRAM, throughput, and output quality on a fixed prompt set.
- [ ] You have a side-by-side FP16 vs quantized table (VRAM, throughput, quality).
- [ ] You identified at least one prompt class where quantization hurt quality.
- [ ] You can state when quantization is free lunch vs a hidden quality tax.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
