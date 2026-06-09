---
type: "week"
week: 41
phase: "Phase 5 — Networking, Distributed Systems for AI, Distributed Training"
status: "not-started"
start: 
end: 
objective: "Synthetic data & training/eval data pipelines: streaming systems, dedup, filtering, synthetic gen."
concepts: ["[[Queueing and Backpressure]]"]
project: []
deliverable: 
tags: ["week", "phase/5"]
---

# Week 41 — Synthetic data & training and eval data pipelines

**Phase:** [[Phase 5 — Networking, Distributed Systems for AI, Distributed Training]]  
**Objective:** Synthetic data & training/eval data pipelines: streaming systems, dedup, filtering, synthetic gen.  
**Concepts:** [[Queueing and Backpressure]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
A data-engine / synthetic-data overview (e.g. from Scale AI / open datasets like FineWeb).

## Read (15m)
A "how we built our data pipeline" engineering post.

## Build (20m)
Build a small streaming pipeline that ingests, dedups, filters, and tokenizes a corpus at throughput; measure tokens/sec.

## Step-by-step
1. Pick a raw corpus (e.g. a slice of FineWeb or your own data).
2. Build a streaming pipeline: ingest → dedup → filter → tokenize, processing in a stream not a batch.
3. Measure end-to-end throughput in tokens/sec and find the bottleneck stage.
4. Add a synthetic-generation or augmentation step and re-measure.

## Reflect (5m)
> Why is the data pipeline often the real bottleneck in training, not the GPUs?

## Done when
- [ ] A streaming pipeline with a measured tokens/sec throughput.
- [ ] The bottleneck stage identified.
- [ ] You can explain why data pipelines, not GPUs, are often the training bottleneck.

## Common pitfalls
- Exact dedup is cheap; near-dedup (MinHash/embeddings) is where cost and quality really live.
- If the pipeline can't feed the GPUs at training speed, your expensive GPUs sit idle.

## Resources
- [[Designing Machine Learning Systems]]
- [[Databricks (Mosaic) Engineering]]

## Go deeper
- A data-engine / synthetic-data overview (Scale AI, FineWeb).
- A "how we built our data pipeline" engineering post.

## Tasks
- [ ] Study/open [[Designing Machine Learning Systems]]
- [ ] Study/open [[Databricks (Mosaic) Engineering]]
- [ ] **Build:** Build a small streaming pipeline that ingests, dedups, filters, and tokenizes a corpus at throughput; measure tokens/sec.
- [ ] A streaming pipeline with a measured tokens/sec throughput.
- [ ] The bottleneck stage identified.
- [ ] You can explain why data pipelines, not GPUs, are often the training bottleneck.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
