---
type: "concept"
area: "[[Inference Infrastructure]]"
difficulty: 3
mastery: 0
prerequisites: ["[[KV Cache]]", "[[GPU Memory Hierarchy]]"]
unlocks: ["[[RadixAttention and Prefix Caching]]"]
tags: ["concept", "area/inference-infrastructure"]
---

# PagedAttention

vLLM's technique: store the KV cache in fixed-size blocks (like OS virtual-memory paging) instead of one contiguous buffer per sequence. This kills fragmentation, enables near-100% KV memory use, and makes sharing/copy-on-write of prefixes possible.

> [!info] Why it matters for an infra engineer
> It's the OS-paging idea you already know, applied to GPU memory. It's why vLLM can pack far more concurrent sequences onto a GPU.

## Related

- **Area:** [[Inference Infrastructure]]
- **Prerequisites:** [[KV Cache]], [[GPU Memory Hierarchy]]
- **Unlocks:** [[RadixAttention and Prefix Caching]]
- **Studied in:** [[Week 04 — The KV cache]], [[Week 10 — vLLM in depth]]
- **Resources:** [[vLLM Blog — PagedAttention]], [[PagedAttention (vLLM)]], [[vllm]]
- **Projects:** [[Level 1 — Run local LLMs]]

## Notes
