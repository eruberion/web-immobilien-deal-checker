# Changelog

Alle bemerkenswerten Aenderungen am Immobilien Deal Checker werden in dieser Datei festgehalten.

Format: [Keep a Changelog](https://keepachangelog.com/de/1.1.0/)
Versionierung: [Semantic Versioning](https://semver.org/lang/de/)

## [Unreleased]

- Design-Compass auf den aktuellen Single-File-Scope, konservative Annahmen und Advice-Boundary der Deal-Einordnung nachgezogen.

## [0.11.1] - 2026-07-18

- Projektstand nach dem versehentlichen OpenClaw-Rollback wiederhergestellt und gegen den Referenz-Commit vor dem Rollback baumidentisch validiert.
- Restore-Stand mit HTML-/JavaScript-, DOM-, Versions-, Client-only- und Berechnungs-Smoke-Tests geprueft; Details stehen in `docs/RESTORE_QA_2026-07-18.md`.
- Veraltete README-Verweise auf nicht versionierte historische Dateien entfernt und den lokalen QS-Nachweis verlinkt.
- Gespiegelte OpenClaw-Web-Skills wieder bytegenau mit der zentralen `skills-source` synchronisiert und den neuen Fachskill `immobilien-deal-expert` aufgenommen.
- Zentrale Closeout-Dokumentation workspace-relativ referenziert, damit die Regeln auf mehreren Rechnern ohne Benutzerpfad-Aenderungen gelten.
- Versionierte Pre-Commit-/Pre-Push-Proxies fuer die zentrale OpenClaw-Governance ergaenzt.
- `PRODUCT.md` als fachlicher Produkt-Steckbrief mit Scope, Grenzen, Erfolgskriterien und Advice-Boundary für Immobilien-Plausibilisierung ergänzt.
- `VERSION` als Repo-Level-SemVer-Quelle eingefuehrt; HTML-Meta und sichtbare Versionsanzeige bleiben Versionsspiegel.
- Die Projektstruktur erstmals als persistenter Graphify-Wissensgraph mit Auditbericht, interaktiver HTML-Ansicht und Integritaetspruefung dokumentiert.

## [0.11.0] - 2026-03-31

- SemVer-Baseline fuer den bestehenden Stand `immobilien-deal-checker-v11.html` angelegt.
- Lokale Projekt-Doku und Changelog eingefuehrt.
