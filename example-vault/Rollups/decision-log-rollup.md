# Decision log (roll-up)

Every decision from every meeting note, newest first. Works on hand-written notes from these templates and on notes
Stilltone exports (`Stilltone/Meetings/`). Needs the Dataview plugin.

```dataview
TABLE WITHOUT ID L.text AS "Decision", file.link AS "Meeting", date AS "Date"
FROM ""
WHERE type = "meeting"
FLATTEN file.lists AS L
WHERE meta(L.section).subpath = "Decisions"
SORT date DESC
```

Stilltone also writes one note per memory to `Stilltone/Memories/`. Its "Where things stand" section lists only the
decisions that still stand; replaced ones are already removed.
