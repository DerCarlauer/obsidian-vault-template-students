<%*
const PATH = "/Karriere/Studium"
const AUTHOR = "?"
const STUDENT = AUTHOR + " (Matr. Nr.: ????)"
//const MODULES = ["Information Security", "Big Data"]
const LECTURERS = ["Dozent:in 1", "Dozent:in 2", "Dozent:in 3"]
const CATEGORIES = ["Vorlesung","Selbststudium", "Sonstiges", "Tutorium", "Übung", "Notiz", "Zusammenfassung"]

/*
Diese Vorlage ist für das Studium gedacht. Damit sie immer aktuell ist, müssen die Konstanten überhalb dieses Kommentars regelmäßig gepflegt werden.

PATH: Dieses Skript legt neue Dokumente an einem Ziel Ort ab. Also in einem Ordner innerhalb des Obsidian Walls. Mit der Konstante "path" wird der Pfad zum Ziel-Ordner definiert. Z.B.: "/Ebene1/Ebene2/Ziel-Ordner/"

AUTHOR: Hier sollte der Name des Eigentümers des Obsidian Vault stehen. Z.B.: "Kim Mustermensch"

LECTURERS: Hier können die Dozenten:innen hinterlegt werden, die während des Studiums relevant werden. Z.B.: ["Teacher1", "Teacher2"]

CATEGORIES Für jedes Modul gibt es unterschiedliche Anlässe, für welche man ein Dokument erstellen will. Diese Anlässe können hier in den Kategorien definiert werden. Z.B.: ["Vorlesung","Selbststudium", "Sonstiges", "Tutorium", "Übung"]

*/

//Felder werden alphabetisch sortiert:
if (tp.file.title == "Untitled" || tp.file.title == "Unbenannt")  {
	var module = (await tp.system.prompt("Modul Bezeichnung:")).trim()
} else {
	var module = tp.file.title
}

var lecturers = LECTURERS.sort()
var categories = CATEGORIES.sort()

//Dropdown Menüs werden geöffnet und Werte zugewiesen:
var lecturer = (await tp.system.suggester(lecturers, lecturers, false, "Dozent:in:", 50)).trim()
var category = (await tp.system.suggester(categories, categories, false, "Art:", 50)).trim()

//Für die Hashtags werden Leerzeichen entfernt und alles in Kleinbuchstaben umgewandelt:
var tagModule = module.replace(/ /g, '_').toLowerCase()
var tagCategory = category.replace(/ /g, '_').toLowerCase()

var dateYyyymmdd = tp.date.now("YYYY-MM-DD")
var dateDdmmyyyy = tp.date.now("DD.MM.YYYY")

//Erstelle Dokumentname und Dateiname:
var documentName = module + " - " + category
fileName = dateYyyymmdd + " " + documentName

//Benenne Datei und verschiebe sie in den Zielordner:
await tp.file.rename(fileName)
await tp.file.move(PATH + "/" + module + "/"+ fileName)
-%>
---
lecturer: <% lecturer %>
module:  <% module %>
topic:
document_date: <% dateDdmmyyyy %>
note_title: <% documentName %>
note_type: document
note_creation_date: <% tp.date.now("YYYY-MM-DD") %>
note_creation_time:  <% tp.date.now("HH:mm:ss") %>
note_author: "<% AUTHOR %>"
tags: [ " #studium/<% tagModule %> ", " #<% tagCategory %> " ]

---
# <% documentName %>
#studium/<% tagModule %>  #<% tagCategory %>
Dozent:in: <% lecturer %>
Student:in: <% STUDENT %>
Datum: <% dateDdmmyyyy %>

---
