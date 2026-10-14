# Decisions by project (roll-up)

Every decision, grouped by the meeting's `project` property, newest first. Needs Dataview.

```dataview
TABLE WITHOUT ID L.text AS "Decision", file.link AS "Meeting", date AS "Date"
FROM ""
WHERE type = "meeting" AND project
FLATTEN file.lists AS L
WHERE meta(L.section).subpath = "Decisions"
SORT project ASC, date DESC
```

One project only (replace the name):

```dataview
TABLE WITHOUT ID L.text AS "Decision", file.link AS "Meeting", date AS "Date"
FROM ""
WHERE type = "meeting" AND project = "Atlas launch"
FLATTEN file.lists AS L
WHERE meta(L.section).subpath = "Decisions"
SORT date DESC
```
