# Meeting templates for Obsidian (and plain Markdown)

Free meeting-note templates with Dataview roll-ups that collect **every decision** and **every open action item**
across your meeting notes. They follow the same note shape Stilltone writes when it exports meetings to Obsidian, so
the roll-ups work on hand-written notes and on Stilltone notes alike.

| Template | For |
|---|---|
| `templates/meeting-minutes.md` | Formal minutes: agenda, decisions, action items, open questions |
| `templates/meeting-notes.md` | Quick notes for any meeting |
| `templates/one-on-one-meeting.md` | 1:1s, with "since last time" |
| `templates/weekly-meeting-notes.md` | Recurring meetings |
| `templates/decision-log.md` | A decision log table (current / replaced) |
| `templates/action-item-tracker.md` | An action item table |
| `templates/meeting-follow-up-email.md` | The follow-up email |
| `templates/ai-notetaker-policy.md` | A policy template for teams using AI note takers |
| `rollups/decision-log-rollup.md` | Dataview: every decision across meetings, newest first |
| `rollups/action-items-rollup.md` | Dataview: every open action item, grouped by meeting (+ one person's) |

## Use
1. Copy `templates/` into your vault's templates folder (core **Templates** plugin: `{{title}}` and `{{date}}` fill in).
2. Install the community **Dataview** plugin and copy `rollups/` into your vault.

**The shape the roll-ups rely on:** frontmatter `type: meeting` and `date: YYYY-MM-DD`; decisions as list items under
`## Decisions`; action items as tasks under `## Action Items` (`- [ ] what — Owner (due: …)`).
Tested with Obsidian 1.14 and Dataview 0.5.68.

Stilltone writes these notes automatically from your calls, on your Mac: https://stilltone.app

MIT License.
