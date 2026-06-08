---
type: "concept"
area: "[[Inference Infrastructure]]"
difficulty: 4
mastery: 0
prerequisites: ["[[TTFT vs ITL]]", "[[Queueing and Backpressure]]"]
unlocks: ["[[AI Cost Engineering]]"]
tags: ["concept", "area/inference-infrastructure"]
---

# Inference Autoscaling

QPS-based autoscaling is *wrong* for LLMs (variable input/output lengths). You scale on SLO-relevant signals — TTFT, queue depth, KV utilization, decode-token rate — and with disaggregation you autoscale prefill and decode pools **separately**.

> [!info] Why it matters for an infra engineer
> Getting the scaling signal right is the difference between meeting SLOs and burning money. This is the everyday knob of cost-efficient serving.

## Related

- **Area:** [[Inference Infrastructure]]
- **Prerequisites:** [[TTFT vs ITL]], [[Queueing and Backpressure]]
- **Unlocks:** [[AI Cost Engineering]]
- **Studied in:** [[Week 29 — Inference on Kubernetes — KServe & Ray]], [[Week 30 — Disaggregated serving — Dynamo & llm-d]]
- **Resources:** [[kserve]], [[kuberay]]
- **Projects:** [[Level 4 — AI platform on Kubernetes]], [[Level 6 — Distributed inference cluster]]

## Notes
