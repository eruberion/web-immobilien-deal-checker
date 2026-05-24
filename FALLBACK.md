# FALLBACK.md — Immobilien Deal Checker

## Wenn der Deal Checker nicht erreichbar ist

Der Immobilien Deal Checker ist eine statische Single-File-HTML-App. Keine laufenden Server-Prozesse.

### Sofortcheck

1. Browser-Cache leeren und Seite neu laden.
2. Provider-Status prüfen (je nach aktivem Deployment-Ziel).
3. DNS-Ausbreitung abwarten bei kürzlichen DNS-Änderungen (bis 48h möglich).

### Recovery

Da die App eine einzige HTML-Datei ist:

- **Lokale Kopie:** `immobilien-deal-checker.html` direkt im Browser öffnen.
- **Neuaufschaltung:** Bei Provider-Ausfall die Datei bei alternativem Hosting hochladen.
- **GitHub Pages Fallback:** Repo kann kurzfristig über GitHub Pages published werden.

Alle Berechnungen laufen client-seitig im Browser. Keine Nutzerdaten werden serverseitig gespeichert.

## Deployment-Ziel

> TBD — noch nicht final entschieden. Dieser Abschnitt wird nach Deploy-Entscheidung ergänzt.
