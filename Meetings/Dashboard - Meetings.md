---
buttons: "`button-meeting-neu-1`"
note_type: Level 1 Dashboard
note_author: DerCarlauer
note_date_creation: 2023-05-04 22:05:62
tags:
  - "#dashboard"
---

[Obsidian - Home](../Obsidian%20Vault%20Administration/Obsidian%20-%20Home.md)  | `button-meeting-neu-1`
![](../Obsidian%20Vault%20Administration/Obsidian%20-%20Bilder/people%20having%20a%20meeting%20psychodelic.png)

```dataview
	table WITHOUT ID
	link(file.link, title) AS "meetings", thema, teilnehmende from "Meetings" 
	WHERE contains(note_type, "Meeting")
	sort datum asc
```
