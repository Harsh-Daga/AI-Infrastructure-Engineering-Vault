---
type: "week"
week: 11
phase: "Phase 2 — LLM Serving, Deep"
status: "not-started"
start: 
end: 
objective: "SGLang & RadixAttention: automatic prefix caching, when shared-prefix workloads win big."
concepts: ["[[RadixAttention and Prefix Caching]]"]
project: []
deliverable: 
tags: ["week", "phase/2"]
---

# Week 11 — SGLang & RadixAttention

**Phase:** [[Phase 2 — LLM Serving, Deep]]  
**Objective:** SGLang & RadixAttention: automatic prefix caching, when shared-prefix workloads win big.  
**Concepts:** [[RadixAttention and Prefix Caching]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
SGLang docs + the RadixAttention blog.

1. Read the SGLang docs + the RadixAttention blog.
2. Understand how a radix tree shares KV across requests with common prefixes.
3. Write the workload property that makes prefix caching win.

## Read (15m)
SGLang vs vLLM benchmark posts (note the workload-dependence of the result).

1. Read an SGLang-vs-vLLM benchmark post.
2. Note how the winner changes with the workload.
3. Write why a benchmark number without a workload is meaningless.

## Build (20m)
Construct a shared-prefix workload (same long system prompt, many queries); compare SGLang vs vLLM TTFT.

## Step-by-step
1. Install SGLang and serve the same model you used for vLLM.
2. Construct a shared-prefix workload: one long system prompt + many short, varied queries.
3. Measure TTFT and throughput on SGLang with RadixAttention prefix caching on.
4. Run the identical workload on vLLM (with and without prefix caching) and compare.
5. Vary the shared-prefix fraction (10% → 90%) and chart where caching starts to win.

## Reflect (5m)
> What property of your workload decides whether prefix caching matters?

## Done when
- [ ] You have an SGLang-vs-vLLM TTFT comparison on a shared-prefix workload.
- [ ] You can state the workload property that decides whether prefix caching matters.
- [ ] You found the prefix-fraction threshold where caching pays off.

## Common pitfalls
- If prefixes don't actually match (whitespace/template differences), the cache never hits.
- Benchmark wins are workload-dependent — a low shared-prefix workload shows little difference.

## Resources
- [[SGLang Documentation]]
- [[RadixAttention (SGLang)]]
- [[sglang]]
- [[SGLang Blog]]

## Go deeper
- The RadixAttention blog + SGLang docs.
- An SGLang-vs-vLLM benchmark post (note the workload caveats).

## Tasks
- [ ] Study/open [[SGLang Documentation]]
- [ ] Study/open [[RadixAttention (SGLang)]]
- [ ] Study/open [[sglang]]
- [ ] Study/open [[SGLang Blog]]
- [ ] **Build:** Construct a shared-prefix workload (same long system prompt, many queries); compare SGLang vs vLLM TTFT.
- [ ] You have an SGLang-vs-vLLM TTFT comparison on a shared-prefix workload.
- [ ] You can state the workload property that decides whether prefix caching matters.
- [ ] You found the prefix-fraction threshold where caching pays off.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
