# Immobilien Deal Checker

Kleines Single-File-Webprojekt zur schnellen Plausibilitaetspruefung von Immobilien-Investments.

## Monetarisierung & Premium-Roadmap

- Detail-Roadmap: [`docs/PREMIUM_ROADMAP.md`](docs/PREMIUM_ROADMAP.md)
- Zielmodell: **Freemium + Monatsabo + Jahresabo**
- Preisempfehlung: **59,99 € / Jahr**
- Monatsabo: **9,99 bis 12,99 €**
- Kein Lifetime am Anfang, weil Saved Deals, Vergleich und laufende Verbesserungen eher zu Subscription passen

## Versionierung

- SemVer fuer Releases: `MAJOR.MINOR.PATCH`
- Aktuelle Release-Version: `0.11.1`
- Source of Truth: `VERSION`; `immobilien-deal-checker.html` spiegelt denselben Wert via `<meta name="app-version" ...>` und sichtbarer Versionsanzeige.
- Die fruehere Dateinamens-Baseline `v11` ist im Changelog der SemVer-Version `0.11.0` zugeordnet; historische Einzeldateien sind nicht Bestandteil dieses Repositories.

## Dateien

- `immobilien-deal-checker.html` — aktueller Stand der Anwendung
- `CHANGELOG.md` — lokale Kurz-Historie
- `docs/RESTORE_QA_2026-07-18.md` — QS-Nachweis des Gegen-Restores

## Pflege-Regel

- Bei sichtbaren oder funktionalen Aenderungen `VERSION` und die HTML-Versionsspiegel aktualisieren
- Passenden Eintrag in `CHANGELOG.md` ergaenzen
- Wenn spaeter weitere HTML-Staende entstehen, Dateiname und SemVer bewusst synchron oder klar dokumentiert halten
