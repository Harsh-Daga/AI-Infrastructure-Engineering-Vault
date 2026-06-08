---
type: "meta"
tags: ["meta"]
---

# Bases — the core-plugin alternative

This vault uses **Dataview** for all dashboards. Obsidian also ships a first-party core plugin called **Bases** (no community install needed) that can replace many of the Dataview *table* views with a database-like, no-code UI.

## When to prefer Bases
- You want a **built-in**, no-plugin-risk solution that ships and is maintained by Obsidian.
- You like editing table data **inline** (change a `status` straight in the grid).
- You're happy with table/card/board views and don't need computed values or JS.

## When to stay on Dataview
- The **DataviewJS** blocks here ([[✅ This Week]]'s active-week finder, the [[📊 Progress Dashboard]] completion %, the by-area buckets in [[🗺️ Resource Library]]) compute things Bases can't express today.
- You want inline queries inside prose.

## How you'd port a view to Bases
1. Enable *Settings → Core plugins → Bases*.
2. Create a `.base` file; add a view with a filter like `file.hasTag("week")`.
3. Add columns bound to the same frontmatter fields this vault already uses (`status`, `phase`, `objective`, `difficulty`, `mastery`, `area`, …). Because every note has consistent frontmatter, Bases works **without any changes to the notes**.

> Recommended: keep Dataview for the JS-driven dashboards, and optionally add a Bases view over `#resource` or `#week` if you prefer editing those in a grid. The frontmatter schema supports both simultaneously.
