---
type: "concept"
area: "[[GPU Orchestration]]"
difficulty: 4
mastery: 0
prerequisites: []
unlocks: ["[[Gang Scheduling]]"]
tags: ["concept", "area/gpu-orchestration"]
---

# DRA

Dynamic Resource Allocation (GA in K8s 1.34): replaces the integer device-plugin model (`nvidia.com/gpu: 1`) with topology-aware, attribute-rich `ResourceClaim`/`ResourceClaimTemplate`/`DeviceClass`/`ResourceSlice` scheduling. NVIDIA donated its DRA driver to the CNCF.

> [!info] Why it matters for an infra engineer
> This is the single rarest hands-on platform skill in 2026, and it's a direct extension of the Kubernetes you already know.

## Related

- **Area:** [[GPU Orchestration]]
- **Unlocks:** [[Gang Scheduling]]
- **Studied in:** [[Week 26 — Dynamic Resource Allocation (DRA)]]
- **Resources:** [[Kubernetes DRA Documentation]], [[AWS — AI on EKS Guide]], [[k8s-dra-driver]], [[CNCF — KubeCon talks]]
- **Projects:** [[Level 4 — AI platform on Kubernetes]]

## Notes
