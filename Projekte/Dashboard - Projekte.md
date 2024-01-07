---
buttons: "`button-project-neu-1`"
note_type: Level 1 Dashboard
note_author: DerCarlauer
note_date_creation: 2023-05-04 22:05:62
tags:
  - "#dashboard"
---

[Obsidian - Home](../Obsidian%20Vault%20Administration/Obsidian%20-%20Home.md) | `button-project-neu-1`

![](../Obsidian%20Vault%20Administration/Obsidian%20-%20Bilder/projectmanagement.png)


```dataview
	table WITHOUT ID link(file.link, note_title) as Projekt, tags as Tags from "Projekte" WHERE note_type = "project" SORT note_title asc
```


