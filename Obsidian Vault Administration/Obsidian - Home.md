---
tags:
  - "#dataview"
note_author: DerCarlauer
note_date_creation: 2023-05-05 9:51:49
---

![](Obsidian%20-%20Bilder/obsidian_home_header.jpeg)

# Dashboards
```dataview
table WITHOUT ID link(file.link, title) AS "Dashboards", buttons AS Buttons from #dashboard WHERE note_type = "Level 1 Dashboard" sort file.name asc
```

----

## Nicht zugewiesene Tasks
``` tasks
not done
NOT (tags include #mensch )
```



----

# Obsidian Administration
Hier findet ihr Dateien, welche Teil der Vault Infrastruktur sind:

```dataview
table tags from #admin/obsidian 
```
