---
type: "dashboard"
tags: ["dashboard"]
---

# 📄 Papers Tracker

> The Part 7.6 mandatory papers (read the architecture + results, skip the proofs) plus any other papers you add.

## Mandatory papers — read/unread split (Dataview)
<!-- Requires Dataview. The mandatory reading list with status. -->
```dataview
TABLE author AS "Author", status AS "Status", difficulty AS "Diff", why AS "Why"
FROM #paper AND #mandatory
SORT status ASC, file.name ASC
```

## Mandatory papers checklist (Dataview TASK view alternative)
<!-- Requires Dataview. Unread mandatory papers only. -->
```dataview
LIST why
FROM #paper AND #mandatory
WHERE status != "done"
```

## All papers (Dataview)
```dataview
TABLE author AS "Author", area AS "Area", status AS "Status", rating AS "★"
FROM #paper
SORT status ASC
```
