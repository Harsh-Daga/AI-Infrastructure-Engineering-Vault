---
type: "concept"
area: "[[AI Networking]]"
difficulty: 3
mastery: 0
prerequisites: []
unlocks: ["[[Collective Communication (NCCL)]]", "[[FlashAttention]]", "[[GPU Profiling]]", "[[GPU Sharing (MIG and MPS)]]", "[[KV Cache]]", "[[KV Offload]]", "[[NVLink and NVSwitch]]", "[[PagedAttention]]", "[[Quantization]]", "[[ZeRO and FSDP]]"]
tags: ["concept", "area/ai-networking"]
---

# GPU Memory Hierarchy

GPUs have a steep memory hierarchy: registers → shared memory/L1 → L2 → HBM (VRAM), with bandwidth dropping at each tier. Decode is **memory-bandwidth-bound** (you stream the whole model + KV per token); prefill is **compute-bound** (big matmuls). This is the CPU cache/NUMA story re-anchored: map L1/L2/RAM to shared-mem/L2/HBM, and "memory bandwidth, not FLOPs, bounds decode."

> [!info] Why it matters for an infra engineer
> Whether a workload is compute- or memory-bound decides every serving and hardware decision. This is your home turf, re-pointed at HBM.

## Related

- **Area:** [[AI Networking]]
- **Unlocks:** [[Collective Communication (NCCL)]], [[FlashAttention]], [[GPU Profiling]], [[GPU Sharing (MIG and MPS)]], [[KV Cache]], [[KV Offload]], [[NVLink and NVSwitch]], [[PagedAttention]], [[Quantization]], [[ZeRO and FSDP]]
- **Studied in:** [[Week 05 — GPU architecture & memory hierarchy]]
- **Resources:** [[Horace He — Making Deep Learning Go Brrrr]], [[Programming Massively Parallel Processors]], [[Computer Architecture — A Quantitative Approach]], [[Horace He & PyTorch Talks]]

## Notes
