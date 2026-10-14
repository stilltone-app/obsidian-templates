# Open action items (roll-up)

Every unfinished action item from every meeting note, grouped by meeting, newest first. Needs the Dataview plugin.

```dataview
TASK
FROM ""
WHERE type = "meeting" AND !completed AND meta(section).subpath = "Action Items"
GROUP BY file.link
SORT file.frontmatter.date DESC
```

Only one person's items (replace the name):

```dataview
TASK
FROM ""
WHERE type = "meeting" AND !completed AND meta(section).subpath = "Action Items" AND contains(text, "— Anna")
```
