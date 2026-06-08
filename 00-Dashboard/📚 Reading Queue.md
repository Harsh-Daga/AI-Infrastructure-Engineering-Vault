---
type: "dashboard"
tags: ["dashboard"]
---

# 📚 Reading Queue

## To read — easiest first (Dataview)
<!-- Requires Dataview. The core reading queue, sorted so you can pick a quick win or a deep dive. -->
```dataview
TABLE resource-kind AS "Kind", difficulty AS "Diff", area AS "Area", why AS "Why it matters"
FROM #resource
WHERE status = "to-read"
SORT difficulty ASC
```

## Currently reading (Dataview)
```dataview
TABLE resource-kind AS "Kind", author AS "Author", area AS "Area"
FROM #resource
WHERE status = "reading"
SORT file.name ASC
```

## Recently finished (Dataview)
```dataview
TABLE rating AS "★", date-done AS "Done", area AS "Area"
FROM #resource
WHERE status = "done"
SORT date-done DESC
```
