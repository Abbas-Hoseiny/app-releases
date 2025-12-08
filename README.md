# Pflanzenschutz App - Releases

Dieses Repository enthält die Release-Dateien für die Pflanzenschutz Desktop App.

## Aktuelle Version

**Version 2.0.1** - 8. Dezember 2025

### Änderungen in v2.0.1

- Bugfix: Import-Funktion speichert Daten korrekt in SQLite
- Bugfix: Archiv-Logs zeigen korrekten Eintrag-Count
- Neu: EU 2023/564 & QS-GAP Compliance Artikel
- Neu: Schnellstart-Anleitung
- Korrigierte Info-Texte

## Downloads

| Plattform             | Download |
| --------------------- | -------- |
| **Windows**           | [Pflanzenschutz-2.0.1-win.exe](https://github.com/Abbas-Hoseiny/app-releases/releases/download/v2.0.1/Pflanzenschutz-2.0.1-win.exe) |
| macOS (Apple Silicon) | [Pflanzenschutz-2.0.1-mac-arm64.dmg](https://github.com/Abbas-Hoseiny/app-releases/raw/main/Pflanzenschutz-2.0.1-mac-arm64.dmg) |
| macOS (Intel)         | [Pflanzenschutz-2.0.1-mac-x64.dmg](https://github.com/Abbas-Hoseiny/app-releases/raw/main/Pflanzenschutz-2.0.1-mac-x64.dmg) |

## Installation

### Windows

1. EXE-Datei herunterladen
2. Doppelklick auf die EXE
3. **Fertig!** (Portable App - keine Installation nötig)

> **Hinweis:** Windows SmartScreen zeigt möglicherweise eine Warnung. Klicke auf "Weitere Informationen"  "Trotzdem ausführen"

### macOS

1. DMG-Datei herunterladen
2. Doppelklick zum Öffnen
3. App in den Applications-Ordner ziehen
4. **Wichtig:** Beim ersten Start wird die App möglicherweise blockiert

#### Falls "App ist beschädigt" erscheint:

**Option 1:** Terminal öffnen und ausführen:

`ash
xattr -cr /Applications/Pflanzenschutz.app
`

Dann die App normal starten.

**Option 2:**

1. Rechtsklick auf die App  "Öffnen"
2. Im Dialog auf "Öffnen" klicken

**Option 3:**

1. Systemeinstellungen  Datenschutz & Sicherheit
2. Unten bei "Sicherheit" auf "Trotzdem öffnen" klicken

## Updates

Die App prüft automatisch auf Updates. Wenn eine neue Version verfügbar ist, erscheint ein Dialog mit Download-Link.

## Support

Bei Fragen oder Problemen: **Abbas Hoseiny**

## Datenschutz

Alle Benutzerdaten werden **lokal** auf dem Gerät gespeichert und niemals übertragen.
Die Update-Prüfung ruft nur die latest.json Datei ab, ohne persönliche Daten zu senden.
