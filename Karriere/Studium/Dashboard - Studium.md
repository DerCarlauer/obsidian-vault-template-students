---
buttons: "`button-studium-modul-1`"
note_type: Level 1 Dashboard
note_author: DerCarlauer
note_date_creation: 2023-08-04 09:42:49
tags:
  - "#dataview"
  - "#dashboard"
  - "#studium"
---

[Obsidian - Home](../Obsidian%20Vault%20Administration/Obsidian%20-%20Home.md) 

```button
name Neues Studium Modul
type note(Unbenannt) template
action Vorlage Studium - Dashboard Level 2
color blue
```
^button-studium-modul-1

```dataview
	table WITHOUT ID link(file.link, module) as "Modul", semester as Semester, buttons as Buttons from #studium
	WHERE note_type = "Level 2 Dashboard" sort semester desc, file.name	asc
```
