# Pflanzenschutz App - Releases

Dieses Repository enthält die Release-Dateien für die Pflanzenschutz Desktop App.

## Aktuelle Version

**Version 2.0.0** - 7. Dezember 2025

## Downloads

| Plattform             | Download                                                                                                                                        |
| --------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| macOS (Apple Silicon) | [Pflanzenschutz-2.0.0-mac-arm64.dmg](https://github.com/Abbas-Hoseiny/app-releases/releases/download/v2.0.0/Pflanzenschutz-2.0.0-mac-arm64.dmg) |
| macOS (Intel)         | [Pflanzenschutz-2.0.0-mac-x64.dmg](https://github.com/Abbas-Hoseiny/app-releases/releases/download/v2.0.0/Pflanzenschutz-2.0.0-mac-x64.dmg)     |
| Windows               | [Pflanzenschutz-2.0.0-win.exe](https://github.com/Abbas-Hoseiny/app-releases/releases/download/v2.0.0/Pflanzenschutz-2.0.0-win.exe)             |

## Installation

### macOS

1. DMG-Datei herunterladen
2. Doppelklick zum Öffnen
3. App in den Applications-Ordner ziehen
4. Beim ersten Start: Rechtsklick → Öffnen (wegen Gatekeeper)

### Windows

1. EXE-Datei herunterladen
2. Installer ausführen
3. Installationsanweisungen folgen

## Updates

Die App prüft automatisch auf Updates. Wenn eine neue Version verfügbar ist, erscheint ein Dialog mit Download-Link.

## Für Entwickler

### Neues Release erstellen

1. **Version in `package.json` erhöhen**
2. **Build erstellen:**
   ```bash
   npm run dist:mac   # macOS
   npm run dist:win   # Windows
   ```
3. **GitHub Release erstellen:**
   - Tag: `vX.X.X`
   - Dateien hochladen
4. **`latest.json` aktualisieren:**
   ```json
   {
     "version": "X.X.X",
     "releaseDate": "YYYY-MM-DD",
     "notes": "Release Notes",
     "downloads": {
       "mac-x64": "...",
       "mac-arm64": "...",
       "win": "..."
     }
   }
   ```
5. **Commit & Push**

## Datenschutz

Alle Benutzerdaten werden **lokal** auf dem Gerät gespeichert und niemals übertragen.
Die Update-Prüfung ruft nur die `latest.json` Datei ab, ohne persönliche Daten zu senden.
