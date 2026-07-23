# Bewerbungs-Tracker

Ein einfacher, lokaler Bewerbungs-Tracker als einzelne HTML-Datei. Keine Installation nötig — einfach im Browser öffnen.

## Funktionen

### Stellenverwaltung
- Stellenangebote hinzufügen, bearbeiten und löschen
- Status verfolgen: Neu, Entwurf fertig, Beworben, Vorstellungsgespräch, Abgelehnt
- Arbeitsmodell kennzeichnen: Remote, Hybrid, Vor Ort
- Notizen und Links pro Stelle
- Filtern nach Status

### Suche
- Echtzeit-Suchfeld in der Toolbar
- Durchsucht Stellentitel, Unternehmen, Standort und Notizen
- Sofortige Ergebnisse beim Tippen

### Lebenslauf hochladen
- PDF, DOCX oder TXT hochladen — der Text wird automatisch ausgelesen
- Alternativ: Lebenslauf-Text manuell einfügen
- Wird lokal im Browser gespeichert (einmalig hochladen genügt)

### Texte generieren (AI-Prompts)
Für jede Stelle können drei verschiedene Prompts generiert werden, die den Lebenslauf und die Stellendaten kombinieren:

- **Anschreiben** — vollständiges Bewerbungsanschreiben
- **📧 E-Mail** — kurzer E-Mail-Text (3–5 Sätze), um Lebenslauf und Anschreiben als Anhang anzukündigen
- **📋 Portal-Text** — kompakter Begleittext (4–6 Sätze) für das Freitextfeld in einem Online-Bewerbungsportal

Die generierten Prompts können per Klick kopiert und in Claude, ChatGPT oder ein anderes AI-Tool eingefügt werden.

### Daten-Export & -Import
- Excel-Export (.xlsx) aller Stellen
- Excel-Import zum Wiederherstellen oder Teilen von Daten
- CSV-Fallback, falls SheetJS nicht verfügbar ist

## Nutzung

**Online (GitHub Pages):**  
Öffne die GitHub Pages-Seite direkt im Browser — keine Installation nötig.

**Offline:**  
Lade `index.html` herunter und öffne die Datei in einem beliebigen Browser.

**Desktop-App (.exe):**  
Siehe den Ordner `desktop/` für Anweisungen zum Bauen einer portablen Windows-App mit Electron.

## Projektstruktur

```
bewerbungs-tracker/
├── index.html          ← GitHub Pages (Web-Version)
├── README.md           ← Diese Datei
└── desktop/
    ├── main.js         ← Electron-Hauptprozess
    ├── index.html      ← Tracker für die Desktop-App
    ├── package.json    ← Build-Konfiguration
    └── README.md       ← Bauanleitung für die .exe
```

## Technische Details

- Einzelne HTML-Datei, kein Backend, kein Framework
- Daten werden im `localStorage` des Browsers gespeichert
- Externe Bibliotheken (via CDN): [SheetJS](https://sheetjs.com/) (Excel), [Mammoth.js](https://github.com/mwilliamson/mammoth.js) (DOCX), [PDF.js](https://mozilla.github.io/pdf.js/) (PDF)

## Hinweise

- Daten bleiben pro Browser gespeichert — beim Wechsel des Browsers oder Computers den Excel-Export/Import nutzen
- Keine Registrierung, kein Server, keine Kosten
- Der Lebenslauf verlässt den Browser nicht — alles bleibt lokal
