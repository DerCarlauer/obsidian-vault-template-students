---
buttons: "`button-zettelkasten-neu-1`"
note_type: Level 1 Dashboard
note_author: DerCarlauer
note_date_creation: 2023-05-04 22:05:62
tags:
  - "#dashboard"
---

[Obsidian - Home](../Obsidian%20Vault%20Administration/Obsidian%20-%20Home.md) | `button-zettelkasten-neu-1` | [Was ist ein Zettelkasten?](https://de.wikipedia.org/wiki/Zettelkasten)

![zettelkasten psychodelisch](../Obsidian%20Vault%20Administration/Obsidian%20-%20Bilder/zettelkasten%20psychodelisch.png)
```dataview
	table WITHOUT ID link(file.link, note_title) as Zettel, tags as Tags from "Zettelkasten" WHERE note_type = "zettel" SORT note_title asc
```


