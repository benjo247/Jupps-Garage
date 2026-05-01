# Jupp's Garage Webseite

Statische Webseite mit eingebundenem WerkstattLoop-Buchungstool.

## Was ist neu in v3

- Inline-Buchungstool **komplett entfernt** (war redundant)
- Stattdessen: **Modal-Embedding** über `werkstattloop.vercel.app/embed.js`
- Buttons mit `data-werkstattloop="jupps-garage"` öffnen automatisch das Modal
- Fahrzeugschein-Upload + DSGVO-Konsens läuft jetzt zentral auf werkstattloop
- Sticky CTA-Button auf Mobile für maximale Conversion

## Wie das Embedding funktioniert

```html
<!-- Jeder Button mit data-werkstattloop öffnet das Modal -->
<button data-werkstattloop="jupps-garage">Termin buchen</button>

<!-- Das Script vor </body> einbinden -->
<script src="https://werkstatt-loop.vercel.app/embed.js" async></script>
```

Das Script:
- Findet alle Buttons mit `data-werkstattloop="..."`
- Bei Klick: öffnet ein Modal-Overlay
- Im Modal: Iframe lädt `/r/jupps-garage?embed=1`
- Buchung wird zentral verarbeitet, landet in WerkstattLoop-Dashboard
- Modal schließt nach erfolgreicher Buchung automatisch

## Deploy

Push zum verbundenen Vercel-Projekt → Auto-Deploy.

Keine Build-Steps, keine Dependencies — pure HTML mit CDN-Tailwind.
