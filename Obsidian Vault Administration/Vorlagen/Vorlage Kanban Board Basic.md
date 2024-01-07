<%*
var author = "?"
if (tp.file.title == "Untitled" || tp.file.title == "Unbenannt")  {
	// Wenn die Datei gerade neu erzeugt wurde, hat sie noch keinen definierten Titel, er muss nachgefragt werden
	var noteTitle = "Kanban Board - " + await tp.system.prompt("Bezeichnung des Kanban Boards:")
	await tp.file.rename(noteTitle)
	await tp.file.move("/Projekte/Kanban Boards/" + noteTitle)
} else {
	// Wenn die Datei aus einem Link erzeugt wurde, hat sie den Linknamen als Dateinamen
	var projectId = tp.file.title
	var noteTitle = "Kanban Board - " + projectId
	await tp.file.rename(noteTitle)
	await tp.file.move("/Projekte/" + projectId + "/" + noteTitle)
}
-%>
---

kanban-plugin: basic
note_author:  <% author %>
note_title: <% noteTitle %>
note_type: kanban board
note_creation_date: <% tp.date.now("YYYY-MM-DD") %>
note_creation_time:  <% tp.date.now("HH:mm:ss") %>
project_id: <% projectId %>

---

## Backlog



## Planed



## In progress



## Done





%% kanban:settings
```
{"kanban-plugin":"basic"}
```
%%