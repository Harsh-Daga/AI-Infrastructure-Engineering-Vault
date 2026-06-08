---
type: "permanent"
date: "2026-06-09"
tags: ["permanent"]
---

# Inference is a memory-movement problem, not a FLOPs problem

_My own synthesized idea._

## The idea
Decode latency is set by how fast you can stream the model weights + KV cache out of HBM, not by how many FLOPs the GPU can do. Every serving win — [[Quantization]], [[PagedAttention]], [[KV Offload]], [[FlashAttention]] — is ultimately a way to move *less* memory or move it *closer*.

## Why it holds
Per decode step you re-read the whole model and the growing KV; arithmetic intensity is low, so you're bandwidth-bound (see [[GPU Memory Hierarchy]]).

## Connects to
- [[Prefill vs Decode]] · [[KV Cache]] · [[TTFT vs ITL]]
