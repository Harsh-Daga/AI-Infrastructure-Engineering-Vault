---
type: "area"
ranked: "yes"
demand: 5
comp: 5
depth: 4
difficulty: 4
longevity: 5
tags: ["area", "area/ai-platform-engineering"]
---

# AI Platform Engineering

> Building the internal paved road for AI workloads.

## Part 1 ranking (1–5)
| Demand | Comp | Depth | Difficulty | Longevity |
|---|---|---|---|---|
| 5 | 5 | 4 | 4 | 5 |

## Resources

- [[AI Engineering]]
- [[Designing Machine Learning Systems]]
- [[AWS — AI on EKS Guide]]
- [[Databricks (Mosaic) Engineering]]
- [[Modal, Replicate, Anyscale, BentoML & W&B Blogs]]
- [[kuberay]]
- [[kserve]]
- [[The Batch (DeepLearning.AI)]]
- [[Latent Space (newsletter & podcast)]]
- [[Dwarkesh Podcast]]
- [[MLOps Community Podcast]]
- [[The TWIML AI Podcast]]

## Live view (DataviewJS)
<!-- Requires the Dataview plugin. Lists every note tagged to this area automatically. -->
```dataviewjs
const slug = "area/ai-platform-engineering";
const pages = dv.pages("#" + slug).sort(p => p.type);
dv.table(["Note", "Type", "Difficulty", "Status/Mastery"],
  pages.map(p => [p.file.link, p.type, p.difficulty ?? "",
    p.status ?? (p.mastery !== undefined ? "mastery " + p.mastery : "")]));
```
