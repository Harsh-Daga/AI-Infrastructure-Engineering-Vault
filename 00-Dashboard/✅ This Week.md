---
type: "dashboard"
tags: ["dashboard"]
---

# ✅ This Week

> [!warning] Seeing raw code instead of a live dashboard?
> Install the **Dataview** community plugin, then enable **Settings → Dataview → Enable JavaScript Queries**.
> Also switch to **Reading view** or **Live Preview** (not Source mode). See [[README — How to use this vault]] for the full setup.

## The active week

```dataviewjs
const weeks = dv.pages("#week").sort(w => w.week, "asc");
let active = weeks.find(w => w.status === "in-progress");
if (!active) {
  const doneWeeks = weeks.filter(w => w.status === "done");
  const lastDoneNum = doneWeeks.length ? Math.max(...doneWeeks.map(w => w.week)) : 0;
  active = weeks.find(w => w.week === lastDoneNum + 1);
}
if (!active) { dv.paragraph("🎉 All 52 weeks are done."); }
else {
  const statusLabel = active.status === "not-started" ? "next up (not yet started)" : active.status;
  dv.header(2, active.file.link);
  dv.paragraph(`**Phase:** ${active.phase} · **Status:** ${statusLabel}`);
  dv.paragraph(`**Objective:** ${active.objective}`);
  if (active.concepts) dv.paragraph("**Concepts:** " + active.concepts.join(", "));
  const tasks = active.file.tasks.where(t => !t.completed);
  if (tasks.length) { dv.header(3, "Open tasks"); dv.taskList(tasks, false); }
  else dv.paragraph("_No open tasks — mark this week done and the next will surface here._");
}
```

## How to use
1. Mark your current week `status: done` (+ `end:` date) when finished.
2. The next week automatically appears here — no need to set it to `in-progress`.
3. Do **Learn → Read → Build → Reflect**, tick tasks, log in a Daily note.
4. Repeat — just mark each week `done` when finished.