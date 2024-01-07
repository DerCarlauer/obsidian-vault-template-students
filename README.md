# obsidian-vault-template-students
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
## Infos zu unserem Obsidian Vault
Damit kollaboratives Arbeiten realistischer wird, brauchen wir gute Templates und eine gute Struktur in unserem Vault. Wir lösen dass, indem wir für jede Kategorie ein Dashboard gebaut haben:
[Dashboard - Studium](Karriere/Studium/Dashboard%20-%20Studium.md), [Dashboard - Meetings](Meetings/Dashboard%20-%20Meetings.md), [Dashboard - Menschen](Menschen/Dashboard%20-%20Menschen.md), [Dashboard - Projekte](Projekte/Dashboard%20-%20Projekte.md), [Dashboard - Tagesnotizen](Tagesnotizen/Dashboard%20-%20Tagesnotizen.md), [Dashboard - Zettelkasten](Zettelkasten/Dashboard%20-%20Zettelkasten.md)

Innerhalb der Dashboards findest du Buttons, mit denen du entsprechende Seiten erstellen kannst. In den Vorlagen, die durch die Buttons aufgerufen werden, haben wir Skripte hinterlegt, die hilfreiche Informationen hinterlegen und weitere Struktur schaffen.

Zudem haben wir eine Startseite definiert: [Obsidian - Home](Obsidian%20Vault%20Administration/Obsidian%20-%20Home.md)
Auf der Startseite werden alle Dashboards mit dem Plugin Dataview automatisch angezeigt. Und damit wir zudem sehr schnell zur Startseite gelangen, haben wir einen Hotkey dafür definiert: CMD-H
## Erste Schritte
Sobald du dieses Vault heruntergeladen und geöffnet hast, empfehlen wir die folgende Vorgehensweise.
### 1. Community Erweiterungen installieren und aktivieren
Damit dieses Vault Sinn macht, raten wir zur Installation und Nutzung der unten aufgelisteten Community Plugins. Jedoch musst du vorher die Nutzung von Community Plugins aktivieren. Gehe dafür zu "Preferences/Externe Erweiterungen":
![community_erweiterung_1](Obsidian%20Vault%20Administration/README%20Anhänge/community_erweiterung_1.png)
Installiere und aktiviere danach die folgenden Plugins:
* [Buttons](https://github.com/shabegom/buttons)
* [Dataview](https://github.com/blacksmithgu/obsidian-dataview)  
* [Hotkeys for specific files](https://github.com/Vinzent03/obsidian-hotkeys-for-specific-files)
* [Excalidraw](https://github.com/zsviczian/obsidian-excalidraw-plugin)
* [Kanban](https://github.com/mgmeyers/obsidian-kanban)
* [Tasks](https://github.com/obsidian-tasks-group/obsidian-tasks)
* [Templater](https://github.com/SilentVoid13/Templater)

**Achtung**: Achte darauf, dass Du die Erweiterungen nicht nur installierst, sondern auch aktivierst. Das sieht dann so aus:
![community_erweiterung_2](Obsidian%20Vault%20Administration/README%20Anhänge/community_erweiterung_2.png)
### 2. Community Erweiterungen konfigurieren
Damit alles so funktioniert, wie wir es uns gedacht haben, solltest du folgende Konfigurationen durchführen:
#### Konfiguration des Plugins "Hotkeys for specific files"
Wir wollen schnell von A nach B kommen. Dafür brauchen wir die Startseite. Gehe zu den Einstellungen des Plugins "Hotkeys for specific files" und füge die Datei [Obsidian Vault Administration/Obsidian - Home](Obsidian%20Vault%20Administration/Obsidian%20-%20Home.md) hinzu:
![hotkey_home](Obsidian%20Vault%20Administration/README%20Anhänge/hotkey_home.png)
**Achtung**: Diese Änderung wird erst nach einem Neustart von Obsidian wirksam. Nun solltest Du mit dem Tastenkürzel "CMD-H" direkt zur Startseite kommen. Sollte das noch nicht funktionieren, dann konfiguriere es unter der Option "Tastenkürzel"
#### Konfiguration des Plugins "Templater"

![templater_configuration](Obsidian%20Vault%20Administration/README%20Anhänge/templater_configuration.png)


Nun bist du startklar. Probiere alle Buttons auf Seite [Obsidian - Home](Obsidian%20Vault%20Administration/Obsidian%20-%20Home.md) aus, damit du ein Gefühl für die Struktur des Vaults bekommst.
# Tipps und Tricks
## Nützliche Hotkeys
* CMD-H: Wechsel zur Seite [Obsidian - Home](Obsidian%20Vault%20Administration/Obsidian%20-%20Home.md)
* CMD-D: Erstellt eine neue Excalidraw-Datei und öffnet diese in einem neuen Tab. Der Link zur Datei wird gleichzeitig in die vorher aktive Markdown Datei eingefügt.
* CMD-P: Befehlspalette öffnen