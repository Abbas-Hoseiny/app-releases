# Pflanzenschutz App - Releases

Dieses Repository enthält die Release-Dateien für die Pflanzenschutz Desktop App.

## Aktuelle Version

**Version 2.0.1** - 7. Dezember 2025

### Änderungen in v2.0.1

- Bugfix: Import-Funktion speichert Daten korrekt in SQLite
- Bugfix: Archiv-Logs zeigen korrekten Eintrag-Count

## Downloads

| Plattform             | Download                                                                                                                        |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| macOS (Apple Silicon) | [Pflanzenschutz-2.0.1-mac-arm64.dmg](https://github.com/Abbas-Hoseiny/app-releases/raw/main/Pflanzenschutz-2.0.1-mac-arm64.dmg) |
| macOS (Intel)         | [Pflanzenschutz-2.0.1-mac-x64.dmg](https://github.com/Abbas-Hoseiny/app-releases/raw/main/Pflanzenschutz-2.0.1-mac-x64.dmg)     |
| Windows               | _Kommt bald_                                                                                                                    |

## Installation

### macOS

1. DMG-Datei herunterladen
2. Doppelklick zum Öffnen
3. App in den Applications-Ordner ziehen
4. **Wichtig:** Beim ersten Start wird die App möglicherweise blockiert

#### Falls "App ist beschädigt" erscheint:

**Option 1:** Terminal öffnen und ausführen:

```bash
xattr -cr /Applications/Pflanzenschutz.app
```

Dann die App normal starten.

**Option 2:**

1. Rechtsklick auf die App → "Öffnen"
2. Im Dialog auf "Öffnen" klicken

**Option 3:**

1. Systemeinstellungen → Datenschutz & Sicherheit
2. Unten bei "Sicherheit" auf "Trotzdem öffnen" klicken

### Windows

1. EXE-Datei herunterladen
2. Installer ausführen
3. Installationsanweisungen folgen

## Updates

Die App prüft automatisch auf Updates. Wenn eine neue Version verfügbar ist, erscheint ein Dialog mit Download-Link.

## Für Entwickler

### Automatischer Release (empfohlen)

Im `electron` Repository gibt es ein Release-Script:

```bash
cd /pfad/zu/electron
./release.sh "Beschreibung der Änderungen"
```

Das Script:

1. Liest Version aus `package.json`
2. Baut die App
3. Kopiert DMGs hierher
4. Aktualisiert `latest.json`
5. Committed und pusht

### Manueller Release

1. **Version in `package.json` erhöhen**
2. **Build erstellen:**
   ```bash
   npm run dist:mac   # macOS (auf Mac)
   npm run dist:win   # Windows (auf Windows)
   ```
3. **DMGs/EXE hierher kopieren**
4. **`latest.json` aktualisieren:**
   ```json
   {
     "version": "X.X.X",
     "releaseDate": "YYYY-MM-DD",
     "notes": "Release Notes",
     "downloads": {
       "mac-x64": "https://github.com/Abbas-Hoseiny/app-releases/raw/main/Pflanzenschutz-X.X.X-mac-x64.dmg",
       "mac-arm64": "https://github.com/Abbas-Hoseiny/app-releases/raw/main/Pflanzenschutz-X.X.X-mac-arm64.dmg",
       "win": "..."
     }
   }
   ```
5. **Commit & Push**

### Multi-Plattform Release

- **macOS:** Muss auf einem Mac gebaut werden
- **Windows:** Muss auf Windows gebaut werden

Workflow:

1. Version erhöhen → commit & push im `electron` Repo
2. Auf Mac: `git pull` → `npm run dist:mac` → DMGs kopieren
3. Auf Windows: `git pull` → `npm run dist:win` → EXE kopieren
4. `latest.json` aktualisieren (erst wenn ALLE fertig!)
5. Push

## Datenschutz

Alle Benutzerdaten werden **lokal** auf dem Gerät gespeichert und niemals übertragen.
Die Update-Prüfung ruft nur die `latest.json` Datei ab, ohne persönliche Daten zu senden.
