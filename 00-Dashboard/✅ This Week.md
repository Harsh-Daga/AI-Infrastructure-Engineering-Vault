---
type: "dashboard"
tags: ["dashboard"]
---

# ✅ This Week

> [!warning] Seeing raw code instead of a live dashboard?
> Install the **Dataview** community plugin, then enable **Settings → Dataview → Enable JavaScript Queries**.
> Also switch to **Reading view** or **Live Preview** (not Source mode). See [[README — How to use this vault]] for the full setup.

## Current week (works without Dataview)
Until Dataview is installed, work from this embed. When you finish a week, change the link below to the next week (or install Dataview and the block below auto-picks the active week).

![[Week 02 — Tokenization, embeddings, context windows#Tasks]]

---

## The active week (DataviewJS)
<!-- Requires Dataview (JS). Finds the single in-progress week (fallback: lowest-numbered not-started)
     and renders its objective + tasks inline so you can work straight from this note. -->
```dataviewjs
const weeks = dv.pages("#week").sort(w => w.week, "asc");
let active = weeks.find(w => w.status === "in-progress");
if (!active) {
  const lastDone = weeks.filter(w => w.status === "done").sort(w => w.week, "desc")[0];
  const nextNum = lastDone ? lastDone.week + 1 : 1;
  const nextWeek = weeks.find(w => w.week === nextNum);
  if (nextWeek && nextWeek.status !== "done") {
    await nextWeek.file.frontmatter.mutate("status", "in-progress");
    if (!nextWeek.start) await nextWeek.file.frontmatter.mutate("start", dv.date("today"));
    active = nextWeek;
  } else {
    active = weeks.find(w => w.status === "not-started");
  }
}
if (!active) { dv.paragraph("🎉 All 52 weeks are done."); }
else {
  dv.header(2, active.file.link);
  dv.paragraph(`**Phase:** ${active.phase} · **Status:** ${active.status}`);
  dv.paragraph(`**Objective:** ${active.objective}`);
  if (active.concepts) dv.paragraph("**Concepts:** " + active.concepts.join(", "));
  const tasks = active.file.tasks.where(t => !t.completed);
  if (tasks.length) { dv.header(3, "Open tasks"); dv.taskList(tasks, false); }
  else dv.paragraph("_No open tasks — mark this week done and the next will surface here._");
}
```

## How to use
1. Set one week's frontmatter to `status: in-progress` (and fill `start:`).
2. This note pulls its objective, concepts, and unchecked tasks automatically.
3. Do **Learn → Read → Build → Reflect**, tick tasks, log in a Daily note.
4. Set `status: done` (+ `end:`) and the next week appears here.
