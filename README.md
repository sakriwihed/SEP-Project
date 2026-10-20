# Code
Der **Billard Helper** ist eine Android-App, die Billardspieler dabei unterstützt, ihre Spiele zu tracken, Statistiken auszuwerten und Regeln nachzuschlagen. 

## Grobe Projektübersicht
Die App bietet folgende Funktionen:
- **Match-Tracking:** Erfassung von gelochten Bällen, Fouls und Aufnahmen (Innings) im Einzel oder Teammodus.
- **Statistik:** Visualisierung der Spielerleistung über Zeiträume hinweg mithilfe von Diagrammen.
- **Profilverwaltung:** Erstellung und Verwaltung lokaler Spielerprofile.
- **Regelbuch:** Ein integriertes Regelbuch für die Billard-Varianten 8-Ball, 9-Ball, 10-Ball, 14.1
- **Leaderboards:** Ranking der besten Spieler basierend auf Siegen und anderen Werten.

## Paketstruktur
Das Projekt ist in verschiedene Pakete unterteilt:
- **`ui`**: Enthält Jetpack Compose Screens, Komponenten und das Design (Theme, Color, Type).
- **`model`**: Definiert die grundlegenden Datenstrukturen.
- **`logic`**: Beinhaltet die Spiellogik, Punktberechnungen und mehr.
- **`vision`**: Beinhaltet die Kamera-Integration und Bildverarbeitungsalgorithmen zur Erkennung der Tischsituation sowie die Geschwindigkeitserkennung beim Anstoß (Break Speed).
- **`data`**: Zuständig für die Datenhaltung, den CSV-Export und die Beständigkeit.

## Sonstige Informationen
- **Sprache:** Kotlin
- **Android-Version:** Mindestens Android 16.0 (API Level 36)
- **Hinweis zu Berechtigungen:** Die App kann grundsätzlich ohne Kamera-, Mikrofon- oder Dateizugriff genutzt werden. Um die vollen Funktionen der App zu nutzen, werden diese Berechtigungen aber vorausgesetzt.
 
