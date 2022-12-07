tags: #daily
creation date: [[<% tp.file.creation_date("YYYY-MM-DD dddd") %>]] <% tp.file.creation_date("HH:mm:ss") %>
description::

<< [[<% tp.date.now("YYYY-MM-DD dddd", -1, tp.file.title, "dddd, MMM D") %>]] | [[<% tp.date.now("YYYY-MM-DD dddd", 1,tp.file.title, "dddd, MMM D") %>]] >> 

---

## {{date:dddd, MMM D}}

### Today's Fleeting Notes
[[Fleeting Notes/{{date:YYYY-MM-DD}} CSCI243]]
[[Fleeting Notes/{{date:YYYY-MM-DD}} MATH211]]
[[Fleeting Notes/{{date:YYYY-MM-DD}} CHIN309]]

[[Fleeting Notes/{{date:YYYY-MM-DD}} CSCI301]]
[[Fleeting Notes/{{date:YYYY-MM-DD}} JAPN208]]
[[Fleeting Notes/{{date:YYYY-MM-DD}} CSCI232]]

---

### Timery
```toggl
LIST FROM {{date:YYYY-MM-DD}} TO {{date:YYYY-MM-DD}}
GROUP BY PROJECT
SORT DESC
```