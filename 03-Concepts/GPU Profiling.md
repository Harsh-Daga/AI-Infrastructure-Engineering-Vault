---
type: "concept"
area: "[[LLM Serving]]"
difficulty: 4
mastery: 0
prerequisites: ["[[GPU Memory Hierarchy]]"]
unlocks: []
tags: ["concept", "area/llm-serving"]
---

# GPU Profiling

You don't write kernels — you *read* them. Profiling (Nsight Systems, PyTorch profiler, nvidia-smi dmon, nvtop) tells you where time actually goes: data movement, a slow kernel, or Python/host overhead. "GPU at 100% utilization" can still be wasteful if it's busy moving memory instead of computing.

> [!info] Why it matters for an infra engineer
> Reading a profile honestly is how you find the real bottleneck instead of guessing. Utilization is a liar; the profiler is not.

## Related

- **Area:** [[LLM Serving]]
- **Prerequisites:** [[GPU Memory Hierarchy]]
- **Studied in:** [[Week 07 — Where the GPU time goes — profiling]]
- **Resources:** [[Horace He — Making Deep Learning Go Brrrr]], [[NVIDIA Deep Learning Institute (DLI)]], [[Horace He & PyTorch Talks]]

## Notes
