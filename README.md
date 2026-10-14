# Meeting templates for Obsidian

**Free meeting-note templates, plus Dataview roll-ups that collect every decision and every open action item across
all your meeting notes.** Write notes by hand with the templates, or let [Stilltone](https://stilltone.app) write them
from your calls. Both use the same note format, so the same roll-ups work for both.

- 8 templates: minutes, quick notes, 1:1s, weekly meetings, a decision log, an action item tracker, a follow-up email,
  and an AI note-taker policy for teams
- 4 roll-ups: decision log, open action items (plus one person's), decisions by project, this week
- An example vault with a made-up project, to see the roll-ups work in two minutes
- Plain Markdown: works in any editor; the roll-ups need Obsidian + Dataview

## What the roll-ups give you

**Decision log** — every decision from every meeting, newest first, with the meeting it came from:

| Decision | Meeting | Date |
|---|---|---|
| Launch moves to 17 March (replaces 3 March) [02:31] | Atlas weekly | 2026-10-07 |
| Launch set for 3 March [04:10] | Atlas kickoff | 2026-10-05 |

**Open action items** — every unfinished task, grouped by meeting; done items drop out:

```
Atlas weekly        ☐ Fix the calendar-step bugs — Ben (due: 2026-10-16)
Atlas kickoff       ☐ Draft the pricing page — Anna (due: 2026-10-10)
```

## Quick start (5 minutes)
1. **Try the example first (optional):** in Obsidian, *Open folder as vault* → `example-vault/`, install Dataview
   (step 3), and open `Rollups/`.
2. **Templates:** copy `templates/` into your vault (for example to `Templates/`). Turn on the core **Templates**
   plugin (Settings → Core plugins → Templates) and set *Template folder location* to that folder. New note →
   *Insert template*: `{{title}}` and `{{date}}` fill in.
3. **Dataview:** Settings → Community plugins → turn off Restricted mode → Browse → **Dataview** → Install → Enable.
4. **Roll-ups:** copy `rollups/` into your vault and open them. They scan every note with `type: meeting`, wherever it is.

## The templates
| File | Use it for |
|---|---|
| [`meeting-minutes.md`](templates/meeting-minutes.md) | Formal minutes: attendees, agenda, summary, decisions, action items, open questions, next meeting |
| [`meeting-notes.md`](templates/meeting-notes.md) | Quick notes for any meeting |
| [`one-on-one-meeting.md`](templates/one-on-one-meeting.md) | 1:1s: since last time, their topics, your topics, feedback, for next time |
| [`weekly-meeting-notes.md`](templates/weekly-meeting-notes.md) | Recurring meetings: what's still open from last week, updates, decisions that replace earlier ones |
| [`decision-log.md`](templates/decision-log.md) | A table to keep by hand: date, decision, why, who, source, status (current / replaced) |
| [`action-item-tracker.md`](templates/action-item-tracker.md) | A table of action items carried from meeting to meeting |
| [`meeting-follow-up-email.md`](templates/meeting-follow-up-email.md) | The follow-up email: decisions, owners and dates, what's still open |
| [`ai-notetaker-policy.md`](templates/ai-notetaker-policy.md) | A starting policy for teams: allowed tools, consent, retention, admin controls |

## The roll-ups
| File | Shows |
|---|---|
| [`decision-log-rollup.md`](rollups/decision-log-rollup.md) | Every decision across meetings, newest first |
| [`action-items-rollup.md`](rollups/action-items-rollup.md) | Every open action item grouped by meeting, plus a one-person version |
| [`decisions-by-project.md`](rollups/decisions-by-project.md) | Decisions grouped by the `project` property, or one project only |
| [`this-week.md`](rollups/this-week.md) | Decisions and open items from the last 7 days |

## The note format
The roll-ups rely on `type: meeting` + `date` in the frontmatter, and on the section names `## Decisions` (list items)
and `## Action Items` (tasks like `- [ ] What — Owner (due: YYYY-MM-DD)`). Full spec: [docs/note-format.md](docs/note-format.md).

## Customize
- **Filter by folder:** change `FROM ""` to `FROM "Work/Meetings"`.
- **Filter by tag:** add `AND contains(tags, "weekly")` to the `WHERE` line.
- **One person:** change the name in `contains(text, "— Anna")`.
- **Rename sections:** if you rename `## Decisions`, change `"Decisions"` in the queries too.

## With Stilltone
[Stilltone](https://stilltone.app) records your calls on your Mac (no bot), transcribes them and writes each meeting
into your vault in this format, with every decision and action item linked to the moment it was said. It also keeps
a note per project or person with what still stands and what's still open. These roll-ups then run across your whole
meeting history with no typing.

## Compatibility
Tested with Obsidian 1.14 and Dataview 0.5.68: the decision and open-items roll-ups against a vault of real
Stilltone exports plus hand-written notes. Plain Markdown everywhere else.

## Contributing
Issues and pull requests are welcome: better templates, more roll-ups, translations.

## License
[MIT](LICENSE) · Made by [Stilltone](https://stilltone.app)
