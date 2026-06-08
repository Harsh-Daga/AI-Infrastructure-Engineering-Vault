---
type: "project"
level: 4
status: "not-started"
phase: "[[Phase 4 — GPU Orchestration & the AI Platform on Kubernetes]]"
skills: ["[[DRA]]", "[[GPU Sharing (MIG and MPS)]]", "[[Gang Scheduling]]", "[[Inference Autoscaling]]", "[[AI Reliability Engineering]]"]
repos: ["[[k8s-dra-driver]]", "[[gpu-operator]]", "[[KAI-Scheduler]]", "[[kserve]]", "[[kuberay]]"]
success-criteria: "A user can deploy a model with one CRD/command; it autoscales on the right signal; you can show multi-tenant fair-share scheduling and a fleet health dashboard."
tags: ["project", "level/4"]
---

# Level 4 — AI platform on Kubernetes

**Phase:** [[Phase 4 — GPU Orchestration & the AI Platform on Kubernetes]]  
**Weeks:** [[Week 25 — GPUs on Kubernetes — the device-plugin era]], [[Week 26 — Dynamic Resource Allocation (DRA)]], [[Week 27 — GPU sharing — MIG, MPS, time-slicing]], [[Week 28 — AI-aware scheduling & gang scheduling]], [[Week 29 — Inference on Kubernetes — KServe & Ray]], [[Week 30 — Disaggregated serving — Dynamo & llm-d]], [[Week 31 — The internal AI platform (paved road)]], [[Week 32 — GPU node observability with eBPF]]

## Architecture
K8s cluster with NVIDIA GPU Operator + DRA, an AI-aware scheduler (KAI/Volcano), KServe/Ray Serve for autoscaling inference, DCGM + Grafana fleet observability, and a self-serve "deploy a model" golden path.

## Components
DRA driver, scheduler, inference CRD/operator, autoscaler, observability stack, a GitOps deploy path.

## Why it matters
This is *the* AI infra role. Almost no one has hands-on DRA + AI scheduling; you will.

## Skills learned
GPU scheduling, MIG/sharing, AI-aware scheduling, inference autoscaling, platform/paved-road design, fleet observability.

## Skills (concept links)

- [[DRA]]
- [[GPU Sharing (MIG and MPS)]]
- [[Gang Scheduling]]
- [[Inference Autoscaling]]
- [[AI Reliability Engineering]]

## Success criteria
> A user can deploy a model with one CRD/command; it autoscales on the right signal; you can show multi-tenant fair-share scheduling and a fleet health dashboard.

## Repos to study
[[k8s-dra-driver]], [[gpu-operator]], [[KAI-Scheduler]], [[kserve]], [[kuberay]]

## Build log
_Log progress here as you build._


## Tasks
- [ ] Scaffold the repo with a real README and architecture doc
- [ ] Implement the core architecture above
- [ ] Produce the benchmark / cost model that proves the success criteria
- [ ] Write the "what I learned" section and publish to the learning log
