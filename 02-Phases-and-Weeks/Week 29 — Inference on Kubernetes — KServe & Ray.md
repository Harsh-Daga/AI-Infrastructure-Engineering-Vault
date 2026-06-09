---
type: "week"
week: 29
phase: "Phase 4 — GPU Orchestration & the AI Platform on Kubernetes"
status: "not-started"
start: 
end: 
objective: "Inference on Kubernetes: KServe, Ray Serve, KubeRay; autoscaling for inference."
concepts: ["[[Inference Autoscaling]]"]
project: ["[[Level 4 — AI platform on Kubernetes]]"]
deliverable: 
tags: ["week", "phase/4"]
---

# Week 29 — Inference on Kubernetes — KServe & Ray

**Phase:** [[Phase 4 — GPU Orchestration & the AI Platform on Kubernetes]]  
**Objective:** Inference on Kubernetes: KServe, Ray Serve, KubeRay; autoscaling for inference.  
**Concepts:** [[Inference Autoscaling]]
**Project:** [[Level 4 — AI platform on Kubernetes]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
KServe docs; KubeRay + Ray Serve docs.

## Read (15m)
A production "serving LLMs on Kubernetes" reference architecture.

## Build (20m)
Deploy your vLLM model behind KServe or Ray Serve with autoscaling; drive load and watch it scale.

## Step-by-step
1. Install KServe (or KubeRay + Ray Serve) on your GPU cluster.
2. Deploy your vLLM model behind it with an autoscaling policy.
3. Pick the right scaling signal (concurrency / KV utilization / queue depth — not raw QPS).
4. Drive load up and down; watch replicas scale and measure scale-up latency.
5. Tune min/max replicas and scale-to-zero behavior for cold-start cost.

## Reflect (5m)
> Why is QPS-based autoscaling wrong for LLMs, and what should you scale on instead?

## Done when
- [ ] Autoscaling inference deployment that scales under load.
- [ ] You chose and justified a non-QPS scaling signal.
- [ ] You measured scale-up latency and cold-start cost.

## Common pitfalls
- Scaling on QPS misfires for LLMs — a few long generations saturate a replica at low QPS.
- Cold starts (model load) are slow; scale-to-zero trades cost for first-request latency.

## Resources
- [[kserve]]
- [[kuberay]]

## Go deeper
- KServe docs; KubeRay + Ray Serve docs.
- A production "serving LLMs on Kubernetes" reference architecture.

## Tasks
- [ ] Study/open [[kserve]]
- [ ] Study/open [[kuberay]]
- [ ] **Build:** Deploy your vLLM model behind KServe or Ray Serve with autoscaling; drive load and watch it scale.
- [ ] Autoscaling inference deployment that scales under load.
- [ ] You chose and justified a non-QPS scaling signal.
- [ ] You measured scale-up latency and cold-start cost.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
