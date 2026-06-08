---
type: "meta"
tags: ["meta"]
---

# README — How to use this vault

A graph-first Obsidian vault for the 52-week **Top 1% AI Infrastructure Engineer** roadmap. Everything is cross-linked so the graph view reveals real structure: a backbone of concept dependencies, with weeks and resources hanging off them, converging on projects.

## 1. Required & optional plugins
**Required (community plugins):**
- **Dataview** — powers every dashboard and the live tables. Enable *Settings → Community plugins → Browse → Dataview*, then in Dataview settings turn on **Enable JavaScript Queries** (the `dataviewjs` blocks need it).
- **Templater** — the note templates in `_templates/`. Point *Templater → Template folder location* at `_templates/`.

**Optional but recommended:**
- **Tasks** — nicer handling of the `- [ ]` checkboxes in week/project notes.
- **Kanban** — a board view of weeks or projects if you like.
- **Excalidraw** — for the Phase-1 "How an LLM runs on a GPU" diagram and the Level-8 topology diagram (save into `_attachments/`).

To enable: *Settings → Community plugins → turn off Restricted mode → Browse → install → enable*.

## 2. Folder structure
- `00-Dashboard/` — [[🏠 Home]] and the five Dataview dashboards. Start here.
- `01-Roadmap/` — one faithful reference note per Part (1–7) of the source roadmap.
- `02-Phases-and-Weeks/` — six Phase MOCs + the 52 fully-populated week notes.
- `03-Concepts/` — atomic concept notes = the knowledge-graph nodes.
- `04-Projects/` — the Level 1–8 projects.
- `05-Resources/` — Books, Courses-and-Guides, Blogs, Papers, Repos, Media.
- `06-Areas/` — a MOC per ranked area (21) and per emerging area (10).
- `07-Notes/` — your own writing: `Daily/`, `Literature/`, `Permanent/`.
- `_templates/` (Templater), `_attachments/` (images/Excalidraw), `_meta/` (this + [[Tag Taxonomy]]).

## 3. The daily workflow
1. Open [[✅ This Week]] — it auto-finds the in-progress week (or the next not-started one).
2. Do **Learn (20m) → Read (15m) → Build (20m) → Reflect (5m)** from that week note.
3. Create a Daily note (Templater → `daily`) in `07-Notes/Daily/`; jot what you learned + open questions.
4. Tick the week's `- [ ]` tasks as you finish each resource/build step.
5. Update the **mastery** field on the concept notes you touched (0→4). Weak spots surface in [[📊 Progress Dashboard]].
6. When the week is finished, set its `status: done` and fill `end:`. The next week appears in This Week.

## 4. How the knowledge graph is wired
Every concept note declares `prerequisites:` and `unlocks:` as wikilinks — together these form the **dependency DAG** described in [[Part 2 — The Knowledge Dependency Graph]]. Weeks link to the concepts they teach; concepts link to the resources that explain them and the projects that apply them; areas (MOCs) gather concepts/weeks/projects/resources. The result: open Graph view and you see week → concept → resource → project chains.

The two ★ keystone nodes are [[KV Cache]] and [[Collective Communication (NCCL)]] — most paths run through them.

## 5. Recommended graph-view color groups
*Settings → Graph view → Groups* (uses the tag taxonomy):
- `tag:#concept` → blue (the backbone)
- `tag:#resource` → green
- `tag:#week` → orange
- `tag:#project` → red
- `tag:#area` → purple
- `tag:#mandatory` → gold (highlight the must-read papers)

Set "Existing files only" on, and bump link/node size by connections to make the keystones pop.

## 6. Dataview cheat-sheet
Each dashboard query has a comment above it explaining what it does and that it needs Dataview (or DataviewJS). If a dashboard is blank, you most likely haven't enabled JavaScript queries in Dataview settings.
