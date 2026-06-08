---
type: "dashboard"
tags: ["dashboard"]
---

# 🏠 Home

> Your entry point. The 52-week curriculum for becoming a top-1% AI Infrastructure Engineer, as a living, graph-first vault.

> [!tip] First-time setup (2 minutes)
> 1. **Settings → Community plugins** → turn off Restricted mode → **Browse** → install **Dataview** and **Templater** → enable both.
> 2. **Settings → Dataview** → turn on **Enable JavaScript Queries**.
> 3. Open [[✅ This Week]] in **Reading view** — you should see a live week + task list, not a code block.
> Full details: [[README — How to use this vault]].

## ▶ Start here every day
- [[✅ This Week]] — the active week and its tasks
- [[📊 Progress Dashboard]] — weeks, projects, concept mastery
- [[📚 Reading Queue]] — what to read next
- [[🗺️ Resource Library]] — everything by type/area
- [[📄 Papers Tracker]] — the mandatory papers

## 🗺 The roadmap (Part 1–7)
- [[Part 1 — The 2026 Landscape]]
- [[Part 2 — The Knowledge Dependency Graph]]
- [[Part 3 — The 52-Week Daily Plan]]
- [[Part 4 — Progressive Projects]]
- [[Part 5 — Highest Signal-to-Noise Resources]]
- [[Part 6 — Emerging Areas]]
- [[Part 7 — The Top 1% Plan]]

## 🧭 Phases
- [[Phase 1 — Foundations]]
- [[Phase 2 — LLM Serving, Deep]]
- [[Phase 3 — Inference Infrastructure]]
- [[Phase 4 — GPU Orchestration & the AI Platform on Kubernetes]]
- [[Phase 5 — Networking, Distributed Systems for AI, Distributed Training]]
- [[Phase 6 — Reliability, Agents, Scale Simulation & Your Specialization]]

## 🛠 Projects (Level 1 → 8)
- [[Level 1 — Run local LLMs]]
- [[Level 2 — RAG with hybrid search & observability]]
- [[Level 3 — Multi-model routing gateway + cost optimization]]
- [[Level 4 — AI platform on Kubernetes]]
- [[Level 5 — GPU scheduling deep-dive]]
- [[Level 6 — Distributed inference cluster]]
- [[Level 7 — Production-grade AI platform]]
- [[Level 8 — Frontier-scale architecture simulation]]

## 🧠 Knowledge graph
The backbone is the concept DAG in `03-Concepts/` — each node declares `prerequisites:` and `unlocks:`. Open **Graph view**, then color by tag: `#concept` (one color), `#resource` (another), `#week`, `#project`, `#area`. See [[README — How to use this vault]].

The two ★ keystone concepts:
- [[KV Cache]] — ties together attention, memory, and inference.
- [[Collective Communication (NCCL)]] — ties together RDMA, NVLink, and distributed training + inference.

## 📂 Folders
- `01-Roadmap/` · `02-Phases-and-Weeks/` · `03-Concepts/` · `04-Projects/` · `05-Resources/` · `06-Areas/` · `07-Notes/`
- [[README — How to use this vault]] · [[Tag Taxonomy]] · [[Bases — the core-plugin alternative]]

## All weeks (Dataview)
<!-- Requires Dataview. Live list of every week with its status. -->
```dataview
TABLE phase, status, objective
FROM #week
SORT week ASC
```
