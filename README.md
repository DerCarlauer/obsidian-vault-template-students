# obsidian-vault-social-collaboration
## Hintergrund
Dieses Obsidian Vault wurde von [barnes-c](https://github.com/barnes-c), [evelynloe](https://github.com/evelynloe), [tobsebi](https://github.com/tobsebi) & [DerCarlauer](https://github.com/DerCarlauer) erstellt.
Es entstand als Projektarbeit für das Modul "Social Collaboration & Knowledge Management" im Studiengang "Wirtschaftsinformatik" an der [Hochschule Karlsruhe](https://www.h-ka.de/).

Ziel des Projektes war es herauszufinden, wie gut Obsidian genutzt werden kann, wenn man mit mehreren Personen kollaborativ arbeitet und über GitHub synchronisiert.

Wir stellen das Vault, mit dem wir unsere Präsentation vorbereitet haben hier zur Verfügung.
Jedoch haben wir das Plugin [Obsidian Git](https://github.com/denolehov/obsidian-git) entfernt, damit das Vault auch für einzelne Personen ein guter Startpunkt für das Studium ist.
## Kollaboratives Arbeiten
Falls du und dein Team das Vault für kollaboratives Arbeiten nutzen wollt, dann zieht es in ein eigenes gemeinsames Git Repository und installiert zusätzlich noch das Community Plugin [Obsidian Git](https://github.com/denolehov/obsidian-git).
Für ein flüssiges gemeinsames Arbeiten solltet ihr initial eine **.gitIgnore** Datei erstellen, welche die folgenden Zeilen enthält:
`.obsidian/*
!.obsidian/app.json
!.obsidian/appearance.json
!.obsidian/config
!.obsidian/community-plugins.json
!.obsidian/core-plugins.json
!.obsidian/graph.json
!.obsidian/hotkeys.json`
# Infos zu unserem Obsidian Vault

## Konfiguration Empfehlungen
### Community Erweiterungen
Damit kollaboratives Arbeiten realistischer wird, brauchen wir gute Templates und eine gute Struktur in unserem Vault. Wir lösen dass, indem wir für jede Kategorie ein Dashboard gebaut haben:
[Dashboard - Studium](Karriere/Studium/Dashboard%20-%20Studium.md), [Dashboard - Meetings](Meetings/Dashboard%20-%20Meetings.md), [Dashboard - Menschen](Menschen/Dashboard%20-%20Menschen.md), [Dashboard - Projekte](Projekte/Dashboard%20-%20Projekte.md), [Dashboard - Tagesnotizen](Tagesnotizen/Dashboard%20-%20Tagesnotizen.md), [Dashboard - Zettelkasten](Zettelkasten/Dashboard%20-%20Zettelkasten.md)

Zudem haben wir eine Startseite definiert: [Obsidian - Home](Obsidian%20Vault%20Administration/Obsidian%20-%20Home.md)
Auf der Startseite werden alle Dashboards mit dem Plugin Dataview automatisch angezeigt. Und damit wir zudem sehr schnell zur Startseite gelangen, haben wir einen Hotkey dafür definiert: CMD-H
Damit dieses Vault Sinn macht, raten wir zur Installation und Nutzung der folgenden Community Plugins:
* [Buttons](https://github.com/shabegom/buttons)
* [Dataview](https://github.com/blacksmithgu/obsidian-dataview)  
* [Hotkeys for specific files](https://github.com/Vinzent03/obsidian-hotkeys-for-specific-files)
* [Excalidraw](https://github.com/zsviczian/obsidian-excalidraw-plugin)
* [Kanban](https://github.com/mgmeyers/obsidian-kanban)
* [Tasks](https://github.com/obsidian-tasks-group/obsidian-tasks)
* [Templater](https://github.com/SilentVoid13/Templater)
## Erste Schritte
Ein guter Start für einen ersten Überblick ist die Seite [Obsidian - Home](Obsidian%20Vault%20Administration/Obsidian%20-%20Home.md). 
# Tipps und Tricks

> [!info] Nützliche Hotkeys
>  CMD-D: Erstellt eine neue Excalidraw-Datei und öffnet diese in einem neuen Tab. Der Link zur Datei wird gleichzeitig in die vorher aktive Markdown Datei eingefügt.
>  CMD-H: Wechsel zur Seite [Obsidian - Home](Obsidian%20Vault%20Administration/Obsidian%20-%20Home.md)
>  CMD-P: Befehlspalette öffnen