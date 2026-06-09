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

> [!info] How to use this week
> Timebox the four blocks (~60 min/day total). **Learn** builds the model, **Read** grounds it in reality, **Build** makes it real, **Reflect** locks it in. The **Step-by-step** expands the Build; the **Done when** list is your exit criteria.

## Learn (20m)
NVIDIA DCGM exporter docs; an eBPF-for-observability intro (e.g. via Grafana/Pixie-style tooling).

1. Read NVIDIA DCGM exporter docs.
2. Read an eBPF-for-observability intro.
3. List the fleet signals: utilization, ECC, throttling, temp, NVLink.

## Read (15m)
A "GPU fleet observability" engineering post.

1. Read a GPU fleet observability post.
2. Note which signals predicted node failure (Xid, ECC).
3. Write what you'd alert on vs merely chart.

## Build (20m)
Deploy DCGM exporter + Grafana; build a fleet dashboard (utilization, ECC errors, throttling, temp, NVLink); add an eBPF-based trace of one path.

## Step-by-step
1. Deploy the NVIDIA DCGM exporter as a DaemonSet and scrape it with Prometheus.
2. Build a Grafana fleet dashboard: utilization, ECC errors, throttling, temp, power, NVLink BW.
3. Add an eBPF-based trace of one request/syscall path (e.g. via a Pixie-style tool).
4. Inject a fault (or find a noisy node) and see which signals move first.
5. Write the Phase-4 deliverable: platform + scheduling + autoscaling + fleet observability.

## Reflect (5m)
> Which GPU health signals predict an imminent node failure?

## Done when
- [ ] A live GPU fleet dashboard with health signals.
- [ ] An eBPF trace of at least one path.
- [ ] Phase-4 deliverable assembled (Project Level 4).

## Common pitfalls
- Xid errors and ECC counts are leading failure indicators — alert on them, don't just chart them.
- DCGM exporter needs matching driver/DCGM versions or metrics silently go missing.

## Resources
- [[Grafana Labs & Red Hat (OpenShift AI)]]
- [[NVIDIA GPU Operator Documentation]]

## Go deeper
- NVIDIA DCGM exporter docs.
- A "GPU fleet observability" engineering post.

## Tasks
- [ ] Study/open [[Grafana Labs & Red Hat (OpenShift AI)]]
- [ ] Study/open [[NVIDIA GPU Operator Documentation]]
- [ ] **Build:** Deploy DCGM exporter + Grafana; build a fleet dashboard (utilization, ECC errors, throttling, temp, NVLink); add an eBPF-based trace of one path.
- [ ] A live GPU fleet dashboard with health signals.
- [ ] An eBPF trace of at least one path.
- [ ] Phase-4 deliverable assembled (Project Level 4).
- [ ] **Reflect:** answer the week's question in the learning log

## Phase deliverable
> [!success] Phase-4 deliverable: an AI platform on Kubernetes with GPU scheduling, autoscaling inference, and fleet observability (Project Level 4).

## Notes
