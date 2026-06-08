---
type: "meta"
tags: ["meta"]
---

# Tag Taxonomy

A small, consistent tag set. Every note uses these so Dataview queries and graph color-groups stay reliable.

## Note-type tags (exactly one per note)
| Tag | Meaning |
|---|---|
| `#week` | A weekly plan note (`02-Phases-and-Weeks/Week NN`). |
| `#concept` | An atomic concept = a knowledge-graph node (`03-Concepts/`). |
| `#resource` | Any external resource (book/course/blog/paper/repo/media). |
| `#paper` | (implied via `#kind/paper`) a research paper resource. |
| `#project` | A Level 1–8 project (`04-Projects/`). |
| `#area` | An area MOC (`06-Areas/`). |
| `#phase` | A phase MOC. |
| `#dashboard` | A dashboard note (`00-Dashboard/`). |
| `#roadmap` | A Part 1–7 reference note (`01-Roadmap/`). |
| `#daily` / `#literature` / `#permanent` | Your own notes in `07-Notes/`. |

## Modifier tags
| Tag | Meaning |
|---|---|
| `#mandatory` | A Part 7.6 must-read paper. |
| `#emerging` | An emerging-area MOC (Part 6). |
| `#phase/1` … `#phase/6` | Which phase a week or phase note belongs to. |
| `#part/1` … `#part/7` | Which roadmap Part a reference note summarizes. |
| `#level/1` … `#level/8` | A project's level. |
| `#area/<slug>` | The area a concept/resource/area-MOC belongs to (e.g. `#area/inference-infrastructure`). |
| `#kind/<book\|course\|blog\|paper\|repo\|newsletter\|podcast\|youtube>` | A resource's kind. |
| `#status/<to-read\|reading\|done\|reference>` | A resource's reading status (mirrors the `status:` field). |

## Conventions
- **Status** also lives in frontmatter (`status:`) for weeks/projects/resources — the tag is for graph filtering, the field is for Dataview `WHERE`.
- **Mastery** (concepts) and **rating** (resources) are frontmatter-only numbers, not tags.
- Area slugs are lowercase, spaces→`-`, `&`→`and`.
