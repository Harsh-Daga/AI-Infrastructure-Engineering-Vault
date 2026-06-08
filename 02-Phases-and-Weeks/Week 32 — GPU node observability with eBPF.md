---
type: "week"
week: 32
phase: "Phase 4 — GPU Orchestration & the AI Platform on Kubernetes"
status: "not-started"
start: 
end: 
objective: "GPU node observability with eBPF + Prometheus: DCGM exporter, fleet dashboards, health signals."
concepts: ["[[AI Reliability Engineering]]", "[[GPU Profiling]]"]
project: ["[[Level 4 — AI platform on Kubernetes]]"]
deliverable: "Phase-4 deliverable: an AI platform on Kubernetes with GPU scheduling, autoscaling inference, and fleet observability (Project Level 4)."
tags: ["week", "phase/4"]
---

# Week 32 — GPU node observability with eBPF

**Phase:** [[Phase 4 — GPU Orchestration & the AI Platform on Kubernetes]]  
**Objective:** GPU node observability with eBPF + Prometheus: DCGM exporter, fleet dashboards, health signals.  
**Concepts:** [[AI Reliability Engineering]], [[GPU Profiling]]
**Project:** [[Level 4 — AI platform on Kubernetes]]

## Learn (20m)
NVIDIA DCGM exporter docs; an eBPF-for-observability intro (e.g. via Grafana/Pixie-style tooling).

## Read (15m)
A "GPU fleet observability" engineering post.

## Build (20m)
Deploy DCGM exporter + Grafana; build a fleet dashboard (utilization, ECC errors, throttling, temp, NVLink); add an eBPF-based trace of one path.

## Reflect (5m)
> Which GPU health signals predict an imminent node failure?

## Resources
- [[Grafana Labs & Red Hat (OpenShift AI)]]
- [[NVIDIA GPU Operator Documentation]]

## Tasks
- [ ] Study/open [[Grafana Labs & Red Hat (OpenShift AI)]]
- [ ] Study/open [[NVIDIA GPU Operator Documentation]]
- [ ] **Build:** Deploy DCGM exporter + Grafana; build a fleet dashboard (utilization, ECC errors, throttling, temp, NVLink); add an eBPF-based trace of one path.
- [ ] **Reflect:** answer the week's question in the learning log

## Phase deliverable
> [!success] Phase-4 deliverable: an AI platform on Kubernetes with GPU scheduling, autoscaling inference, and fleet observability (Project Level 4).

## Notes
