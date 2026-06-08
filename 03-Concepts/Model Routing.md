---
type: "concept"
area: "[[Model Routing]]"
difficulty: 3
mastery: 0
prerequisites: ["[[TTFT vs ITL]]"]
unlocks: ["[[AI Cost Engineering]]", "[[AI Gateway]]", "[[KV Routing]]"]
tags: ["concept", "area/model-routing"]
---

# Model Routing

Routing each request to the right model by quality/cost/latency — e.g. a cascade (cheap model first, escalate hard prompts). The hard part is deciding *at request time* whether a query is "hard" using a cheap, predictive signal.

> [!info] Why it matters for an infra engineer
> Routing is where you save real money at held quality. It's the everyday control point of a multi-model platform.

## Related

- **Area:** [[Model Routing]]
- **Prerequisites:** [[TTFT vs ITL]]
- **Unlocks:** [[AI Cost Engineering]], [[AI Gateway]], [[KV Routing]]
- **Studied in:** [[Week 21 — Model routing]]
- **Resources:** [[litellm]]
- **Projects:** [[Level 3 — Multi-model routing gateway + cost optimization]]

## Notes
