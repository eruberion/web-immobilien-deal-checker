# Restore-QS vom 18. Juli 2026

## Scope

Validiert wurde ausschliesslich das Repository `web-immobilien-deal-checker` nach dem Gegen-Restore. Die Berechnungs- und UI-Logik blieb unveraendert. Die Pruefung umfasste Git-Baum und Restore-Referenz, Versionsspiegel, HTML-/JavaScript-Struktur, DOM-Verknuepfungen, Client-only-Sicherheitsgrenzen sowie lokale Berechnungs- und Mietspiegel-Smoke-Tests.

## Restore-Bezug

- Gegen-Restore: Pull Request `#6`
- Merge-Commit: `38eb7c53f7263c5b6cdf82ff9b0551597b73620a`
- Referenz vor dem versehentlichen Rollback: `c8a523e`
- Ergebnis des Baumvergleichs: Der durch den Gegen-Restore erzeugte Projektbaum war vor den QS-/Release-Dokumentationsaenderungen identisch mit der Referenz vor dem Rollback.

## Testmatrix

| Pruefung | Ergebnis | Evidenz |
|---|---|---|
| Versionsspiegel | Bestanden | `VERSION`, HTML-Meta, sichtbare Anzeige und README stimmen auf `0.11.1` ueberein |
| JavaScript-Syntax | Bestanden | Inline-Script mit Node `24.18.0` kompiliert |
| DOM-Integritaet | Bestanden | 68 eindeutige IDs; alle 32 per JavaScript referenzierten DOM-Ziele und alle 27 Label-Ziele vorhanden |
| Initialberechnung | Bestanden | VM-Smoke mit den HTML-Standardwerten erzeugt finite Rendite-, Faktor-, LTV-, Cashflow-, Investitions- und AfA-Werte |
| Offenbach-Mietschaetzung | Bestanden | PLZ `63065`, 65 qm und Standardausstattung liefern eine positive Schätzung samt erwarteter Ausgabe |
| Client-only-Grenze | Bestanden | Kein `fetch`, `XMLHttpRequest`, `WebSocket` oder `sendBeacon` im Runtime-Script; keine externe Dependency |
| Lokale Dokumentationsverweise | Bestanden | Veraltete Verweise auf die nicht versionierten Dateien `chat.md` und `immobilien-deal-checker-v11.html` bereinigt |
| HTML-Parser | Bestanden mit Toolhinweis | `xmllint --html --noout` Exit 0; Tidy meldet bekannte Alt-Parser-Warnungen zu HTML5-Elementen, UTF-8 und HTML-Templates im Inline-JavaScript |
| Restore-Baum | Bestanden | Gegen-Restore-Baum entspricht vor den Release-Metadaten dem Commit `c8a523e` |

Beispielwerte des Berechnungs-Smokes: Bruttorendite `4,56 %`, Faktor `21,9x`, LTV `111,57 %`, Gesamtinvestition `278.925,00 EUR` und jaehrliche AfA `4.462,80 EUR`.

## Version-Mapping

| Spiegel | Vorher | Release |
|---|---:|---:|
| `VERSION` | `0.11.0` | `0.11.1` |
| HTML-Meta `app-version` | `0.11.0` | `0.11.1` |
| Sichtbare HTML-Anzeige | `0.11.0` | `0.11.1` |
| `README.md` | `0.11.0` | `0.11.1` |

## Risiken und Grenzen

- Risiko der vorgenommenen Aenderungen: **LOW**. Produktlogik und Berechnungsformeln wurden nicht angefasst.
- Ein interaktiver Browserlauf konnte in der isolierten QS-Umgebung wegen eines Initialisierungsfehlers des Browser-Testadapters nicht ausgefuehrt werden. DOM-Initialisierung, Initialberechnung und Mietschätzung wurden deshalb mit einem isolierten JavaScript-DOM-Smoke ausgefuehrt; ein manueller visueller Release-Smoke bleibt fuer die Deployment-Stufe empfohlen.
- Tidy 5.6 versteht Teile des verwendeten HTML5-/UTF-8-/Inline-Template-Standards nicht vollstaendig. Die Meldungen sind Tool-Kompatibilitaetswarnungen; der tolerantere HTML-Parser und die gezielten Strukturpruefungen waren gruen.
- Die laut Projektregel erforderlichen zentralen Workspace-Dokumente liegen ausserhalb dieses isolierten Produkt-Worktrees und muessen beim Integrations-Closeout separat auf Version `0.11.1` synchronisiert werden.

## Graphify

- Erstaufbau ueber 19 unterstuetzte Dateien: 53 Knoten, 79 gespeicherte Kanten und 9 benannte Communities.
- Single-File-Anwendung, Finanzmodell, Produktgrenzen, Design, Deployment, Premium-Roadmap und Restore-Nachweise wurden semantisch verbunden.
- Persistente Artefakte: `graphify-out/graph.json`, `graphify-out/GRAPH_REPORT.md` und `graphify-out/graph.html`.
- Integritaetsdiagnose: 0 fehlende oder haengende Endpunkte und 0 Self-Loops. Eine gleichgerichtete Parallelbeziehung wurde beim undirektionalen Build erwartungsgemaess zusammengefuehrt.
- Es wurden keine sensitiven Dateien eingelesen und keine externen LLM-API-Schluessel verwendet.
