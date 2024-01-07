---
buttons: "`button-mensch-neu-1`"
note_type: Level 1 Dashboard
note_author: DerCarlauer
note_date_creation: 2023-05-01 9:51:49
tags:
  - "#dataview"
  - "#dashboard"
---

[Obsidian - Home](../Obsidian%20Vault%20Administration/Obsidian%20-%20Home.md) |  `button-mensch-neu-1`
![](../Obsidian%20Vault%20Administration/Obsidian%20-%20Bilder/Colorfull%20community%20looking%20to%20camera.png)

```dataview
table WITHOUT ID
link(file.link, nachname) AS "nachname", link(file.link, vornamen) AS "vornamen" from "Menschen" WHERE note_type = "mensch" sort nachname, vorname desc
```
