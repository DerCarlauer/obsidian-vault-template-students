<%*
if (tp.file.title == "Untitled" || tp.file.title == "Unbenannt")  {
	// Wenn die Datei gerade neu erzeugt wurde, hat sie noch keinen definierten Titel, er muss nachgefragt werden
	var firstName = await tp.system.prompt("Vorname:")
	var lastName = await tp.system.prompt("Nachname:")
	var noteTitle = firstName + " " + lastName
} else {
	// Wenn die Datei aus einem Link erzeugt wurde, hat sie den Linknamen als Dateinamen
	var noteTitle = tp.file.title
}
fileName = noteTitle
await tp.file.rename(fileName)
await tp.file.move("/Menschen/" + fileName)
-%>
---
nachname: <% lastName %>
vornamen: "<% firstName %>"
rufname: <% firstName %>
geburtstag: 
email: 
note_author:
note_type: mensch
note_creation_date: <% tp.date.now("YYYY-MM-DD") %>
note_creation_time:  <% tp.date.now("HH:mm:ss") %>
note_title:  <% noteTitle %>
tags:

---

# <% noteTitle %>
## Notizen


## Kompetenzen


## To Dos
``` tasks <% noteTitle %>
not done
(tags include #mensch/<% (firstName + "_" + lastName).replace(/ /g, '_').toLowerCase() %>) 
```
## Meetings
```dataview
TABLE datum, thema, zusammenfassung
FROM "Meetings"
WHERE note_type = "Meeting" AND contains(teilnehmende, this.file.link) sort datum
```

## Hashtag Erwähnungen in anderen Notizen
Liste aller Notizen mit #mensch/<% (firstName + "_" + lastName).replace(/ /g, '_').toLowerCase() %>
```dataview
TABLE note_type, datum, thema, zusammenfassung
FROM #mensch/<% (firstName + "_" + lastName).replace(/ /g, '_').toLowerCase() %>
WHERE file.name != "<% noteTitle %>" AND note_type != "Meeting"
SORT datum
```
