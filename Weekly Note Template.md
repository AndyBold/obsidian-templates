```
---
created: <% tp.file.creation_date("YYYY-MM-DD") %>
modified: <% tp.file.last_modified_date("YYYY-MM-DD") %>
week-start: <% tp.date.weekday("YYYY-MM-DD", -0) %>
week-end: <% tp.date.weekday("YYYY-MM-DD", 6) %>
---

#weeknotes 

# Tasks

# Completed
```tasks
done after <% tp.date.weekday("YYYY-MM-DD", -0) %>
done before <% tp.date.weekday("YYYY-MM-DD", 6) %>
```

# Day Notes
```dataview
TABLE file.ctime
FROM #daynotes
WHERE file.ctime > date("<% tp.date.weekday("YYYY-MM-DD", -0) %>") and < date("<% tp.date.weekday("YYYY-MM-DD", 6) %>") and !contains(file.name, "-W")
SORT file.ctime ASC
```

# Personal Tracking

```