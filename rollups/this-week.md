# This week (roll-up)

Decisions made and action items still open from meetings in the last 7 days. Needs Dataview.

## Decisions
```dataview
TABLE WITHOUT ID L.text AS "Decision", file.link AS "Meeting", date AS "Date"
FROM ""
WHERE type = "meeting" AND date >= date(today) - dur(7 days)
FLATTEN file.lists AS L
WHERE meta(L.section).subpath = "Decisions"
SORT date DESC
```

## Still open
```dataview
TASK
FROM ""
WHERE type = "meeting" AND !completed AND meta(section).subpath = "Action Items" AND date >= date(today) - dur(7 days)
GROUP BY file.link
```
