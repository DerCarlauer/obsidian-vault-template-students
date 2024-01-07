<%*
console.log("Executing Templater: Vorlage Studium - Dashboard Level 2")

if (tp.file.title == "Untitled" || tp.file.title == "Unbenannt")  {
	var module
	try {	
	  module = await tp.system.prompt("Modul Name (Wichtig: Richtig schreiben.):")
	  if(module == "" || module == null) throw 'Empty variable "module"'
	  } catch (e) {
	  console.log(e)
	  fileName = "Lösch mich"
	  await tp.file.rename(fileName)
	}
} else {
	var module = tp.file.title
}
fileName = "Dashboard - " + module
var buttonModule = module.replace(/ /g, '-')
var tagModule = module.replace(/ /g, '_').toLowerCase()

const PATH = "/Karriere/Studium/" + module + "/"
var buttonName = "Neues Dokument (" + module + ")"
var buttonTypeNote = module
var buttonId = "button-studium-" + buttonModule.toLowerCase() + "-dokument-1"
//Benenne Datei und verschiebe sie in den Zielordner:
await tp.file.rename(fileName)
await tp.file.move(PATH + fileName)

//Die ID des Buttons funktioniert nur, wenn keine Umlaute vorhanden sind. Daher werden diese für die ID entfernt.
function replaceUmlauts(string)
{
    value = string.toLowerCase();
    value = value.replace(/ä/g, 'ae');
    value = value.replace(/ö/g, 'oe');
    value = value.replace(/ü/g, 'ue');
    value = value.replace(/ß/g, 'ss');
    return value;
}
-%>
---
semester:
module:  <% module %>
buttons: "`<% replaceUmlauts(buttonId) %>`"
note_title:  <% fileName %>
note_type: "Level 2 Dashboard"
note_author: "?"
note_creation_date: <% tp.date.now("YYYY-MM-DD") %>
note_creation_time:  <% tp.date.now("HH:mm:ss") %>
tags: [ " #dataview ", " #dashboard ", " #studium/<% tagModule %> " ]

---

#studium/<% tagModule %>

```button
name <% buttonName %>
type note(<% buttonTypeNote %>) template
action Vorlage Studium - Dokument
color green
```
^<% replaceUmlauts(buttonId) %>


```dataview
	table WITHOUT ID link(file.link, note_title) as Dukument, document_date as Datum, lecturer as "Dozent:in", topic as Thema from #studium
	WHERE note_type = "document" AND contains(tags, "#studium/<% tagModule %>") sort file.name	
```
