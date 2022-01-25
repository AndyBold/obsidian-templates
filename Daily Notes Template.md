---
publish: true
created: <% tp.file.creation_date("YYYY-MM-DD") %>
date: <% tp.file.creation_date("YYYY-MM-DD") %>
banner: "![[waves2.png]]"
banner_icon: 📔
---

#daynotes 

<span class="center-element">[Weekday:: [[<% tp.date.now("dddd")  %>]]] | [Yesterday:: [[<% tp.date.now("YYYY-MM-DD", -1)  %>]]] | [Tomorrow:: [[<% tp.date.now("YYYY-MM-DD", +1)  %>]]]
</span>

# Things Written Today
```dataview
list WHERE file.cday = date("<% tp.date.now("YYYY-MM-DD") %>")
```

```button
name New Note
type note(_Inbox/Untitled) template
action 001 - AdHoc Note Template
color yellow
```
^button-9zdx

# ToDo
## Daily Checklist
- [ ] Meditation ⏫ 🛫 <% tp.date.now("YYYY-MM-DD") %> ⏳ <% tp.date.now("YYYY-MM-DD") %> 📅 <% tp.date.now("YYYY-MM-DD") %>
- [ ] Review calendar appointments ⏫ 📅 <% tp.date.now("YYYY-MM-DD")  %>
- [ ] Check email 🔼 📅 <% tp.date.now("YYYY-MM-DD") %>
- [ ] Check Slack 🔼 📅 <% tp.date.now("YYYY-MM-DD")  %>

## Due today
```tasks
not done
due before <% tp.date.now("YYYY-MM-DD", +1)  %>
```

## Due this week
```tasks
not done
due after <% tp.date.weekday("YYYY-MM-DD", 0) %>
due before <% tp.date.weekday("YYYY-MM-DD", 6) %>
```

# Journal

## Log

### Meetings


### Tasks Completed Today
```tasks
done <% tp.date.now("YYYY-MM-DD") %>
```
## Literate DevOps
![[<% tp.date.now("YYYY-MM-DD") %>.org]]

## End of Day Wind-Down 🌙

### Learnings / decisions 💡

### Reflection 🤔

Storyworthy::
Positive::
Negative::
Want to Improve::

Day Rating::
