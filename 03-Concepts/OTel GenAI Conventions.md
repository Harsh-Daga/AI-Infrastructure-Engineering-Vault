---
type: "concept"
area: "[[AI Observability]]"
difficulty: 2
mastery: 0
prerequisites: []
unlocks: ["[[AI Reliability Engineering]]", "[[Eval as Infrastructure]]"]
tags: ["concept", "area/ai-observability"]
---

# OTel GenAI Conventions

The OpenTelemetry `gen_ai.*` semantic conventions: an LLM trace is **just a distributed trace** with extra attributes (model, token counts, cost, cache hit, tool calls). Supported by Langfuse, Phoenix, Datadog, Grafana, etc. Your tracing skills transfer directly.

> [!info] Why it matters for an infra engineer
> This reframes LLM observability as the distributed tracing you already do. Prompt replay + full traces debug things logs cannot.

## Related

- **Area:** [[AI Observability]]
- **Unlocks:** [[AI Reliability Engineering]], [[Eval as Infrastructure]]
- **Studied in:** [[Week 22 — AI observability with OTel GenAI]]
- **Resources:** [[OpenTelemetry GenAI Semantic Conventions]], [[langfuse]], [[phoenix]]
- **Projects:** [[Level 2 — RAG with hybrid search & observability]], [[Level 3 — Multi-model routing gateway + cost optimization]]

## Notes
