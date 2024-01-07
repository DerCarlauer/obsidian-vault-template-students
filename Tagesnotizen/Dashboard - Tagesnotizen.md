---
buttons: Klicke links in der Seitenleiste auf das Kalender Icon
note_author: DerCarlauer
note_creation_date: 2023-05-09
note_creation_time: 08:05:62
note_type: Level 1 Dashboard
tags:
  - "#dashboard"
---

[Obsidian - Home](../Obsidian%20Vault%20Administration/Obsidian%20-%20Home.md)

```dataview
	table WITHOUT ID
	link(file.link, title) AS "Tagesnotizen", zusammenfassung as Zusammenfassung, tags as Tags
	FROM "Tagesnotizen"
	WHERE 
		contains(note_type, "tagesnotiz")
	sort note_date_creation desc
```
