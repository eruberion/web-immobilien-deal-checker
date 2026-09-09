# DEPLOYMENT.md — Immobilien Deal Checker

## Aktueller Betriebsstand

Es ist noch kein öffentliches Deployment freigegeben. Der nachweisbare Stand
ist die lokal ausführbare Single-File-Web-App
`immobilien-deal-checker.html`; sie benötigt keinen Build-Step.

Noch nicht beschlossene Optionen:
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

## Deploy-Regeln (gültig nach einer Deployment-Freigabe)

1. Vor Deploy: lokale Sichtprüfung im Browser.
2. Versionsmeta im HTML aktualisieren (`<meta name="app-version" content="x.y.z">`).
3. CHANGELOG.md bei sichtbaren Änderungen aktualisieren.
4. GitHub bleibt Source of Truth.

## Health-Check

Bis zu einem Livegang gilt der lokale Browser- und QS-Nachweis als technischer
Release-Check. Nach einer Deployment-Freigabe müssen hier die konkrete URL,
ein erfolgreicher HTTPS-Abruf und die zugehörige Provider-/DNS-Prüfung ergänzt
werden. Ein Beispielaufruf ohne erreichbares Ziel ist kein Betriebsnachweis.

## Offene Deployment-Entscheidung

- Provider und Produktdomain sind noch nicht entschieden.
- HTTPS und zentrale Rechtslinks auf `flowhrzn.ai` sind vor einem Livegang
  verpflichtend zu prüfen.
- Diese offenen Punkte sind Freigabegates, keine bereits zugesagten
  Betriebsmerkmale.
