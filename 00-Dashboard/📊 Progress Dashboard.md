---
type: "dashboard"
tags: ["dashboard"]
---

# 📊 Progress Dashboard

## Overall completion (DataviewJS)
<!-- Requires Dataview (JS). Computes % of the 52 weeks marked done. -->
```dataviewjs
const weeks = dv.pages("#week");
const done = weeks.where(w => w.status === "done").length;
const inprog = weeks.where(w => w.status === "in-progress").length;
const pct = Math.round((done / 52) * 100);
dv.paragraph(`**${done} / 52 weeks done (${pct}%)** · ${inprog} in progress`);
dv.el("progress", "", { attr: { value: done, max: 52 } });
```

## Weeks by status (Dataview)
<!-- Requires Dataview. The full week tracker. -->
```dataview
TABLE week AS "Wk", phase AS "Phase", status AS "Status", objective AS "Objective"
FROM #week
SORT week ASC
```

## Projects (Dataview)
<!-- Requires Dataview. Project ladder status. -->
```dataview
TABLE level AS "Lvl", status AS "Status", phase AS "Phase", success-criteria AS "Success criteria"
FROM #project
SORT level ASC
```

## Concept mastery — weak spots first (Dataview)
<!-- Requires Dataview. Sorted ascending so the things you know least surface at the top. -->
```dataview
TABLE area AS "Area", difficulty AS "Diff", mastery AS "Mastery (0-4)"
FROM #concept
SORT mastery ASC, difficulty DESC
```

> **Mastery scale:** 0 unknown · 1 aware · 2 can-explain · 3 can-build · 4 can-teach.
