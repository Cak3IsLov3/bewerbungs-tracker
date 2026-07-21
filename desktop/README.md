# Bewerbungs-Tracker — Desktop-App (.exe) bauen

## Voraussetzungen

- [Node.js](https://nodejs.org/) (Version 18 oder neuer)
- Windows 10/11

## Anleitung

### 1. Projekt vorbereiten

Entpacke diesen Ordner (oder klone das Repo) und öffne ein Terminal im Projektordner:

```bash
cd bewerbungs-tracker-app
```

### 2. Abhängigkeiten installieren

```bash
npm install
```

### 3. App testen (ohne .exe zu bauen)

```bash
npm start
```

Die App öffnet sich als Fenster. Wenn alles funktioniert, weiter mit Schritt 4.

### 4. .exe bauen

```bash
npm run build-win
```

Nach dem Build findest du die portable `.exe` im Ordner `dist/`. Diese Datei kann ohne Installation auf jedem Windows-Computer gestartet werden.

## Dateien

| Datei | Beschreibung |
|-------|-------------|
| `main.js` | Electron-Hauptprozess (öffnet das Fenster) |
| `index.html` | Der Bewerbungs-Tracker (komplette App) |
| `package.json` | Projektdefinition und Build-Konfiguration |

## Hinweise

- Die `.exe` ist eine **portable** Datei — keine Installation nötig, einfach starten
- Daten werden weiterhin lokal im Electron-Storage gespeichert
- Die Dateigröße ist ca. 80–120 MB (Electron enthält einen eingebetteten Browser)
- Optional: Füge eine `icon.png` (256×256 px) hinzu für ein eigenes App-Icon
