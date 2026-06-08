---
type: "dashboard"
tags: ["dashboard"]
---

# 🗺️ Resource Library

> Every resource named in the roadmap, queryable by kind, area, and difficulty.

## Grouped by kind (Dataview)
<!-- Requires Dataview. All resources grouped by their resource-kind. -->
```dataview
TABLE difficulty AS "Diff", area AS "Area", status AS "Status", rating AS "★"
FROM #resource
GROUP BY resource-kind
```

## All resources, by difficulty then kind (Dataview)
```dataview
TABLE resource-kind AS "Kind", area AS "Area", status AS "Status"
FROM #resource
SORT difficulty ASC, resource-kind ASC
```

## By area (DataviewJS)
<!-- Requires Dataview (JS). Buckets resources under each area they touch. -->
```dataviewjs
const res = dv.pages("#resource");
const areas = {};
for (const r of res) {
  for (const a of (r.area ?? [])) {
    const key = (typeof a === "object" && a.path) ? a.path.split("/").pop().replace(".md","") : String(a);
    (areas[key] ??= []).push(r);
  }
}
for (const a of Object.keys(areas).sort()) {
  dv.header(3, a);
  dv.list(areas[a].map(r => r.file.link));
}
```
