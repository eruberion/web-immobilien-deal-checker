# Immobilien Deal Checker

Kleines Single-File-Webprojekt zur schnellen Plausibilitaetspruefung von Immobilien-Investments.

## Monetarisierung & Premium-Roadmap

- Detail-Roadmap: [`docs/PREMIUM_ROADMAP.md`](docs/PREMIUM_ROADMAP.md)
- Die verlinkte Roadmap ist ein historischer, nicht freigegebener
  Hypothesenstand. Abomodell, Preise und Paywall sind keine aktuelle
  Produktentscheidung und duerfen erst nach neuer Markt-, Produkt-,
  Datenschutz- und Advice-Boundary-Pruefung verwendet werden.

## Versionierung

- SemVer fuer Releases: `MAJOR.MINOR.PATCH`
- Aktuelle Release-Version: `0.11.2`
- Source of Truth: `VERSION`; `immobilien-deal-checker.html` spiegelt denselben Wert via `<meta name="app-version" ...>` und sichtbarer Versionsanzeige.
- Die fruehere Dateinamens-Baseline `v11` ist im Changelog der SemVer-Version `0.11.0` zugeordnet; historische Einzeldateien sind nicht Bestandteil dieses Repositories.

## Dateien

- `immobilien-deal-checker.html` — aktueller Stand der Anwendung
- `CHANGELOG.md` — lokale Kurz-Historie
- `docs/RESTORE_QA_2026-07-18.md` — QS-Nachweis des Gegen-Restores

## Pflege-Regel

- Bei sichtbaren oder funktionalen Aenderungen `VERSION` und die HTML-Versionsspiegel aktualisieren
- Passenden Eintrag in `CHANGELOG.md` ergaenzen
- Bei Status-, Versions-, Betriebs- oder Architekturaenderungen die
  kanonische Doku in `finn-workspace` aktualisieren und nach `web-doku`
  synchronisieren; archivierte ZZZ-HTML-/Project-Hub-Seiten nicht reaktivieren
- Wenn spaeter weitere HTML-Staende entstehen, Dateiname und SemVer bewusst synchron oder klar dokumentiert halten
