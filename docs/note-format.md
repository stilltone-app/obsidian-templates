# The meeting note format

The roll-ups read a small, fixed shape. Hand-written notes from these templates and notes exported by
[Stilltone](https://stilltone.app) both follow it, so one set of queries covers both.

## Frontmatter
| Property | Required | Example | Used by |
|---|---|---|---|
| `type` | yes | `meeting` | every roll-up (`WHERE type = "meeting"`) |
| `date` | yes | `2026-10-14` (YYYY-MM-DD) | sorting, "this week" |
| `title` | recommended | `Weekly sync` | display |
| `participants` | optional | `[Anna, Ben]` | your own people queries; Stilltone also writes them as `[[backlinks]]` |
| `project` | optional | `Atlas launch` | `decisions-by-project` |
| `tags` | optional | `[weekly]` | your own filters |

## Sections (level-2 headings, exact names)
| Section | Content | Syntax |
|---|---|---|
| `## Summary` | prose; sub-headings must be `###` or deeper | free text |
| `## Decisions` | one decision per list item; optional source time | `- Launch moves to 17 March [12:31]` |
| `## Action Items` | one task per action item | `- [ ] Update the pricing page — Anna (due: 2026-10-17) [14:02]` |
| `## Open Questions` | one question per list item | `- Windows at launch? — Ben` |
| `## Follow-up` | the follow-up message | free text |

**Rules that keep queries correct**
- Keep the five section names exactly as written; queries match them with `meta(section).subpath`.
- Don't put `##` headings inside a section; use `###`. Otherwise Dataview sees a new section.
- Owners go after an em dash: ` — Name`. Due dates as `(due: YYYY-MM-DD)`.
- Mark a done action item with `- [x]`; the open-items roll-up drops it.

## Notes written by Stilltone
Stilltone writes meetings to `Stilltone/Meetings/` and one note per memory to `Stilltone/Memories/` (`type: memory`,
sections "Where things stand", "Still open", "Sources"). Memory notes are deliberately excluded from the meeting
roll-ups: they already list the decisions that still stand.
