---
type: "concept"
area: "[[LLM Serving]]"
difficulty: 4
mastery: 0
prerequisites: ["[[Prefill vs Decode]]", "[[TTFT vs ITL]]"]
unlocks: []
tags: ["concept", "area/llm-serving"]
---

# Speculative Decoding

A small draft model proposes several tokens; the big model verifies them in one pass, accepting the correct prefix. When acceptance is high it's near-free throughput; when acceptance is low it's wasted compute. Medusa/Eagle are self-drafting variants.

> [!info] Why it matters for an infra engineer
> It's a latency lever whose payoff is workload-dependent. Know when it's free tokens/sec and when it just burns FLOPs.

## Related

- **Area:** [[LLM Serving]]
- **Prerequisites:** [[Prefill vs Decode]], [[TTFT vs ITL]]
- **Studied in:** [[Week 13 — Speculative decoding & latency tricks]]
- **Resources:** [[Speculative Decoding]], [[SGLang Documentation]]

## Notes
