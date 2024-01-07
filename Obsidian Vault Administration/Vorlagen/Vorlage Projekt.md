<%*
if (tp.file.title == "Untitled" || tp.file.title == "Unbenannt")  {
	// Wenn die Datei gerade neu erzeugt wurde, hat sie noch keinen definierten Titel, er muss nachgefragt werden
	var noteTitle = await tp.system.prompt("Bezeichnung des Projektes:")
} else {
	// Wenn die Datei aus einem Link erzeugt wurde, hat sie den Linknamen als Dateinamen
	var noteTitle = tp.file.title
}
await tp.file.rename(noteTitle)
await tp.file.move("/Projekte/" + noteTitle)
-%>
---
note_author: ""
note_title: <% noteTitle %>
note_type: project
note_creation_date: <% tp.date.now("YYYY-MM-DD") %>
note_creation_time:  <% tp.date.now("HH:mm:ss") %>
project_id: <% "project_"+tp.date.now("YYMMDDHHmm") %>
responsible:
priority:
deadline:
goal:
category:
status : #backlog
tags: [ "  " ]

---
# <% noteTitle %>
Projekt ID: <% "project_"+tp.date.now("YYMMDDHHmm") %>
## Projektübersicht
%% Kurze Beschreibung des Projekts und seiner Ziele. %%

## Projektdetails
%% Detaillierte Informationen wie Hintergrund, Kontext und Bedeutung des Projekts. %%

## Projektstatus
%% Aktueller Stand des Projekts, einschließlich Fortschritten, Meilensteinen und ggf. anstehenden Aufgaben. %%

## Team und Verantwortlichkeiten
%% Auflistung der Teammitglieder und ihrer spezifischen Rollen und Verantwortlichkeiten im Projekt. %%

## Kanban Board
```button
name Neues Kanban Board
type note(<% "project_"+tp.date.now("YYMMDDHHmm") %>) template
action Vorlage Kanban Board Basic

```
## Zeitplan und Meilensteine
%% Detaillierter Zeitplan mit Meilensteinen, wichtigen Terminen und Deadlines. %%

## Ressourcen
%% Übersicht über die für das Projekt benötigten oder verwendeten Ressourcen, einschließlich Budget, Materialien und Werkzeuge. %%

## Risikomanagement
%% Identifikation potenzieller Risiken und geplanter Maßnahmen zu deren Bewältigung. %%

## Kommunikationsplan
%% Strategie für die interne und externe Kommunikation, einschließlich regelmäßiger Updates und Berichte. %%

## Dokumentation und Dateien
%% Verweise auf relevante Dokumente, Dateien oder externe Ressourcen, die für das Projekt relevant sind. %%

## Anhänge
%% Zusätzliche Informationen oder Materialien, die für das Verständnis oder die Durchführung des Projekts hilfreich sind. %%