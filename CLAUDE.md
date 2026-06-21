# Immobilien-Deal-Checker – Agent Rules

## OpenClaw Governance

Dieses Projekt wird von OpenClaw gesteuert.
- Governance: light (kein Fastlane, kein UI-Review-Simulator)
- Skills: `react-vite-typescript`, `web-apple-design`, `openclaw-web-premium-ui`, `openclaw-design-system-kickoff`
- `skills/` in diesem Repo ist ein synchronisierter Spiegel aus `Apps/ZZZ_OpenClaw/skills-source/` und wird nicht manuell gepflegt
- Overlay: `Apps/ZZZ_OpenClaw/prompts/projects/immobilien-deal-checker.md`
- Zentrale Projektübersicht: `Apps/ZZZ_OpenClaw/docs/project-hub.html` und `Apps/ZZZ_OpenClaw/docs/project-hub.txt`

## Projekt-Überblick

Immobilien-Deal-Checker ist ein Single-File HTML-Tool zur schnellen Plausibilitätsprüfung von Immobilien-Investments für den deutschen Markt.
**Keine Nutzerdaten verlassen den Browser.**

## Tech Stack

| Technologie | Zweck |
|-------------|-------|
| Vanilla HTML/JS | Gesamte App in einer einzigen Datei |
| CSS-in-HTML | Styling mit Dark Theme |
| HTML5 | Markup und Formular-Logik |

Kein Build-Step notwendig — Datei direkt im Browser öffnen.

## Versionierung

- Source of Truth: `VERSION`; `<meta name="app-version" content="x.y.z">` und sichtbare Versionsanzeige in `immobilien-deal-checker.html` spiegeln denselben Wert.
- Lokale Release-Historie: `CHANGELOG.md`
- Format: `MAJOR.MINOR.PATCH` (SemVer)
- `PATCH`: Bugfix, kleine Korrektur
- `MINOR`: neues rueckwaertskompatibles Feature
- `MAJOR`: Breaking Change / grundlegende Umstrukturierung
- Bei jeder sichtbaren oder funktionalen Aenderung: `VERSION`, HTML-Meta-Tag, sichtbare Versionsanzeige und `CHANGELOG.md` aktualisieren.

## Dokumentations-Pflicht

Bei **jeder Änderung** müssen aktualisiert werden:

1. **`CHANGELOG.md`** – lokaler Kurz-Eintrag unter `Unreleased` bzw. neuer Release-Block
2. **`Apps/ZZZ_OpenClaw/docs/docs-immobilien-deal-checker.html`** – Changelog-Eintrag oben, Stand-Datum im Header
3. **`Apps/ZZZ_OpenClaw/docs/project-hub.html`** und **`Apps/ZZZ_OpenClaw/docs/project-hub.txt`** – Version oder Status in der Immobilien-Deal-Checker-Uebersicht aktualisieren

## Wichtige Regeln

- **Client-only**: Keine externen API-Calls mit Nutzerdaten. Alle Berechnungen laufen lokal im Browser.
- **Berechnungsgenauigkeit**: Finanzberechnungen (ROI, Cashflow, AfA, Tilgung) sind korrekt zu halten. Vor Aenderungen an Formeln immer `immobilien-deal-expert`-Skill laden.
- **Single-File-Prinzip**: Die App bleibt eine einzige HTML-Datei. Kein Build-Tool, kein Node-Setup.
- **Keine externen Dependencies**: Keine CDN-Scripts ohne explizite Freigabe.
- **Kein Push auf `main`**.

## Dateistruktur

```
Immobilien-Deal-Checker/
├── immobilien-deal-checker.html  # Gesamte App (HTML + JS + CSS)
├── README.md
├── CHANGELOG.md
├── skills/                       # OpenClaw Skill-Spiegel (nicht manuell editieren)
├── CLAUDE.md
└── AGENTS.md
```
