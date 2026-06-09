---
type: "week"
week: 22
phase: "Phase 3 — Inference Infrastructure"
status: "not-started"
start: 
end: 
objective: "AI observability with OpenTelemetry GenAI conventions: gen_ai.* traces, token/cost attribution."
concepts: ["[[OTel GenAI Conventions]]"]
project: ["[[Level 2 — RAG with hybrid search & observability]]"]
deliverable: 
tags: ["week", "phase/3"]
---

# Week 22 — AI observability with OTel GenAI

**Phase:** [[Phase 3 — Inference Infrastructure]]  
**Objective:** AI observability with OpenTelemetry GenAI conventions: gen_ai.* traces, token/cost attribution.  
**Concepts:** [[OTel GenAI Conventions]]
**Project:** [[Level 2 — RAG with hybrid search & observability]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
OpenTelemetry GenAI semantic conventions docs; the OTel "Inside the LLM call" blog.

1. Read the OpenTelemetry GenAI semantic conventions.
2. Read the OTel "Inside the LLM call" blog.
3. Write which gen_ai.* attributes you'll put on each span.

## Read (15m)
Langfuse / Arize Phoenix docs; a "LLM trace is just a distributed trace" writeup.

1. Skim Langfuse / Phoenix docs.
2. Note how an LLM trace is just a distributed trace.
3. Write what prompt replay lets you debug that logs can't.

## Build (20m)
Instrument your gateway + RAG with OTel; export to Langfuse or Phoenix; trace one request end-to-end with token/cost on each span.

## Step-by-step
1. Instrument your gateway + RAG with OpenTelemetry using the GenAI semantic conventions.
2. Export traces to Langfuse or Arize Phoenix.
3. Trace one request end-to-end; ensure each span carries token counts and cost.
4. Find a slow/expensive request in the UI and replay its prompt to reproduce.
5. Add cost/token attribution per span so you can see where spend concentrates.

## Reflect (5m)
> What can you debug with a full trace + prompt replay that you cannot with logs alone?

## Done when
- [ ] End-to-end trace of one request with token + cost on each span.
- [ ] You reproduced an issue via prompt replay from a trace.
- [ ] You can name what traces let you debug that logs can't.

## Common pitfalls
- Capturing full prompts/outputs in spans can leak PII — scrub or gate it.
- Missing context propagation breaks the trace into disconnected spans.

## Resources
- [[OpenTelemetry GenAI Semantic Conventions]]
- [[langfuse]]
- [[phoenix]]

## Go deeper
- OpenTelemetry GenAI semantic conventions docs.
- Langfuse / Phoenix tracing docs.

## Tasks
- [ ] Study/open [[OpenTelemetry GenAI Semantic Conventions]]
- [ ] Study/open [[langfuse]]
- [ ] Study/open [[phoenix]]
- [ ] **Build:** Instrument your gateway + RAG with OTel; export to Langfuse or Phoenix; trace one request end-to-end with token/cost on each span.
- [ ] End-to-end trace of one request with token + cost on each span.
- [ ] You reproduced an issue via prompt replay from a trace.
- [ ] You can name what traces let you debug that logs can't.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
