# FALLBACK.md — Immobilien Deal Checker

## Wenn der Deal Checker lokal oder später live nicht erreichbar ist

Der Immobilien Deal Checker ist eine statische Single-File-HTML-App. Keine laufenden Server-Prozesse.

### Sofortcheck im aktuellen, nicht deployten Stand

1. `immobilien-deal-checker.html` direkt im Browser öffnen.
2. Versionsspiegel und den dokumentierten lokalen QS-Pfad prüfen.
3. Erst nach einem freigegebenen Livegang zusätzlich Provider-, DNS-, TLS- und
   HTTP-Status prüfen.

### Recovery

Da die App eine einzige HTML-Datei ist:

- **Lokale Kopie:** `immobilien-deal-checker.html` direkt im Browser öffnen.
- **Neuaufschaltung nach Freigabe:** Den geprüften Stand aus `main` gemäß dem
  dann dokumentierten Provider-Runbook veröffentlichen.
- **Alternativ-Hosting:** GitHub Pages ist nur eine mögliche Option. Es besteht
  keine automatische Failover-Zusage; Domain, HTTPS, Rechtslinks und die
  veröffentlichte Dateiversion müssen vor einer Umschaltung geprüft werden.

Alle Berechnungen laufen client-seitig im Browser. Keine Nutzerdaten werden serverseitig gespeichert.

## Deployment-Ziel

Es gibt noch kein freigegebenes Live-Ziel. `DEPLOYMENT.md` dokumentiert den
lokalen Ist-Stand sowie die vor einem öffentlichen Betrieb erforderlichen
Provider-, Domain-, HTTPS- und Healthcheck-Entscheidungen.
