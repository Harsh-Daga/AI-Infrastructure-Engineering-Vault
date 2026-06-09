---
type: "week"
week: 31
phase: "Phase 4 — GPU Orchestration & the AI Platform on Kubernetes"
status: "not-started"
start: 
end: 
objective: "The internal AI platform (paved road): self-service deploy, golden paths, multi-tenancy, GitOps."
concepts: ["[[Inference Autoscaling]]", "[[AI Reliability Engineering]]"]
project: ["[[Level 4 — AI platform on Kubernetes]]", "[[Level 7 — Production-grade AI platform]]"]
deliverable: 
tags: ["week", "phase/4"]
---

# Week 31 — The internal AI platform (paved road)

**Phase:** [[Phase 4 — GPU Orchestration & the AI Platform on Kubernetes]]  
**Objective:** The internal AI platform (paved road): self-service deploy, golden paths, multi-tenancy, GitOps.  
**Concepts:** [[Inference Autoscaling]], [[AI Reliability Engineering]]
**Project:** [[Level 4 — AI platform on Kubernetes]], [[Level 7 — Production-grade AI platform]]

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
Platform-engineering principles applied to AI; KAITO / AI Runway / BentoML / Anyscale platform overviews.

## Read (15m)
An internal-AI-platform engineering writeup (e.g. how a company built self-serve model serving).

## Build (20m)
Wrap your stack into a one-command/one-CRD "deploy a model" golden path with sane defaults and a dashboard.

## Step-by-step
1. List what an app-engineer/researcher should NOT have to think about (the paved road).
2. Wrap your serving stack behind one CRD or one CLI command with sane defaults.
3. Add GitOps (Argo/Flux) so a model deploy is a PR, and a dashboard for status.
4. Onboard a fake "customer" model end-to-end to prove the golden path.

## Reflect (5m)
> What does a researcher/app-engineer want to not have to think about? Encode that as the paved road.

## Done when
- [ ] One-command/one-CRD "deploy a model" path with sane defaults.
- [ ] GitOps-managed deploys + a status dashboard.
- [ ] A successful end-to-end onboarding of a new model via the paved road.

## Common pitfalls
- A golden path with too many required knobs isn't golden — defaults must cover the common case.
- Self-service without guardrails (quotas, budgets) invites a noisy-neighbor outage.

## Resources
- [[Modal, Replicate, Anyscale, BentoML & W&B Blogs]]
- [[Databricks (Mosaic) Engineering]]

## Go deeper
- Platform-engineering principles applied to AI (paved roads, golden paths).
- KAITO / BentoML / Anyscale internal-platform writeups.

## Tasks
- [ ] Study/open [[Modal, Replicate, Anyscale, BentoML & W&B Blogs]]
- [ ] Study/open [[Databricks (Mosaic) Engineering]]
- [ ] **Build:** Wrap your stack into a one-command/one-CRD "deploy a model" golden path with sane defaults and a dashboard.
- [ ] One-command/one-CRD "deploy a model" path with sane defaults.
- [ ] GitOps-managed deploys + a status dashboard.
- [ ] A successful end-to-end onboarding of a new model via the paved road.
- [ ] **Reflect:** answer the week's question in the learning log

## Notes
