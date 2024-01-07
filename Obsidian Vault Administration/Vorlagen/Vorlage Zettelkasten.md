<%*
if (tp.file.title == "Untitled" || tp.file.title == "Unbenannt")  {
	// Wenn die Datei gerade neu erzeugt wurde, hat sie noch keinen definierten Titel, er muss nachgefragt werden
	var noteTitle = await tp.system.prompt("Titel des Zettels:")
} else {
	// Wenn die Datei aus einem Link erzeugt wurde, hat sie den Linknamen als Dateinamen
	var noteTitle = tp.file.title
}
await tp.file.rename(noteTitle)
await tp.file.move("/Zettelkasten/" + noteTitle)
-%>
---
note_author: ""
note_title: <% noteTitle %>
note_type: zettel
note_creation_date: <% tp.date.now("YYYY-MM-DD") %>
note_creation_time:  <% tp.date.now("HH:mm:ss") %>
zettelkasten_id: <% noteTitle + "_"+tp.date.now("YYMMDDHHmm") %>
tags: [ "  " ]

---
# <% noteTitle %>
## Notizen


## Referenzen

