# Jupp's Garage — Preview

Statische Vorschauseite für Jupp's Garage Baunatal.
Powered by **WerkstattLoop** — Marketing-Add-on für Kfz-Werkstätten.

## Live-Preview

Nach Deploy auf Vercel erreichbar unter `https://<projektname>.vercel.app`.

## Lokal öffnen

Einfach `index.html` doppelklicken — öffnet sich im Browser.
Internetverbindung wird kurz gebraucht (Tailwind/Fonts vom CDN).

## Auf Vercel deployen

1. Repo auf GitHub anlegen, alle Dateien hochladen
2. Auf [vercel.com/new](https://vercel.com/new) Repo importieren
3. **Framework Preset:** Other
4. Alle Build-Settings leer lassen
5. Deploy

Dauert ~30 Sekunden.

## Anpassen

- **Inhalte:** direkt in `index.html` editieren
- **Logo:** `jupps-logo.png` ersetzen (gleicher Dateiname)
- **Farben:** Hex-Codes `#dc2626` (Rot) und `#1e40af` (Blau) per Suchen+Ersetzen ändern

## Struktur

```
.
├── index.html      # Komplette Seite mit Online-Buchungstool
├── jupps-logo.png  # Logo
├── .gitignore
└── README.md
```

Keine Build-Tools, keine Frameworks, keine Abhängigkeiten. Reines HTML/CSS/JS.
