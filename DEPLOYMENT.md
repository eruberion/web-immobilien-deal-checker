# DEPLOYMENT.md — Immobilien Deal Checker

## Aktueller Zielbetrieb

> TBD — Deployment-Ziel noch nicht final entschieden.

Das Projekt ist eine Single-File-Web-App (`immobilien-deal-checker.html`). Kein Build-Step nötig.

Optionen:
- Hostinger klassisches Hosting (statische Datei, kein Node.js nötig)
- GitHub Pages als temporäre Alternative

## Tech Stack

- Single HTML-Datei mit eingebettetem CSS/JS
- Keine Datenbank, keine serverseitige Logik
- Version via `<meta name="app-version" content="...">` im HTML

## Lokale Prüfung

```bash
# Direkt im Browser öffnen
open immobilien-deal-checker.html
```

## Deploy-Regeln (gültig sobald Deployment-Ziel feststeht)

1. Vor Deploy: lokale Sichtprüfung im Browser.
2. Versionsmeta im HTML aktualisieren (`<meta name="app-version" content="x.y.z">`).
3. CHANGELOG.md bei sichtbaren Änderungen aktualisieren.
4. GitHub bleibt Source of Truth.

## Health-Check (gültig sobald live)

> TBD — wird nach Deploy-Entscheidung ergänzt.

## Späterer Zielbetrieb

- Domain: TBD
- HTTPS über Provider-Managed-SSL
- Impressum und Datenschutz auf `flowhrzn.ai` zentral verlinkt
