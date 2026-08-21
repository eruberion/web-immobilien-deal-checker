# Immobilien Deal Checker Design-System V2

Stand: 2026-08-20
Status: verbindliche Designquelle fuer die client-seitige Single-File-Web-App

## Scope und Oberflaechen

Das System gilt fuer:

- Objekt-, Kauf-, Miet-, Finanzierungs-, Kosten- und Steuerformulare
- Mietschätzung, Presets und Bewertungsmodus
- Score, Deal-Meter, Zielbereiche, KPIs und Rechenuebersicht
- Einordnung, Statuspills, Hilfetooltips und Advice-Boundary-Hinweise
- initiale, berechnete, ungueltige, nicht unterstuetzte und fehlerhafte Zustaende

Die App liefert eine konservative Plausibilisierung und Szenariorechnung. Sie ist keine Kaufempfehlung, Finanzierungsaussage, Miet-/Steuer-/Rechtsberatung oder Garantie. Design darf diese Grenze weder durch Ampellogik noch durch starke CTA-Sprache aufweichen.

## Leitidee und Prinzipien

**Serious underwriting desk:** Ein dichter, dunkler Arbeitsbereich, der Annahmen links und nachvollziehbare Ergebnisse rechts gegenueberstellt.

1. Eingabe, Annahme, Rechenergebnis und Einordnung bleiben sichtbar getrennt.
2. Score fasst zusammen, ersetzt aber weder Kennzahlen noch Erklaerung.
3. Farben markieren Pruefstufen, nicht Kaufentscheidungen.
4. Hilfen stehen am Feld; Advice Boundary und Datenbegrenzung bleiben am Ergebnis sichtbar.
5. Die Single-File-Struktur bleibt robust, schnell und ohne externe UI-Abhaengigkeit.

## Farben und semantische Tokens

Implementierungsquelle: der `<style>`-Block in `immobilien-deal-checker.html`.

| Rolle | Token | Wert / Verwendung |
|---|---|---|
| Hintergrund | `--bg` | `#0B1020` |
| Primaerpanel | `--panel` | `#131A2B` |
| Eingabe-/Sekundaerpanel | `--panel-2` | `#1A2238` |
| Primaertext | `--text` | `#EEF2FF` |
| Sekundaertext | `--muted` | `#A7B0C8` |
| Linie | `--line` | `#2B3552` |
| Primaeraktion | `--accent` | `#5C7CFA` |
| Positiver Pruefstatus | `--good` | `#20C997` + Text |
| Pruefhinweis | `--warn` | `#F59F00` + Text |
| Kritischer Pruefstatus | `--bad` | `#FA5252` + Text |
| Schatten | `--shadow` | `0 12px 32px rgba(0,0,0,.25)` |

- `good`, `warn` und `bad` beschreiben Schwellen im gewaehlten Modell, keine Handlungsanweisung.
- Ampelbereiche tragen Text (`Stark`, `Okay`, `Knapp`, `Schwach`) und erklaerbare Kennzahlen.
- Accent bleibt fuer Aktion/Fokus reserviert; fachliche Bewertung verwendet die drei Statusrollen.

## Typografie

- Schriftstack: Inter, `ui-sans-serif`, System UI, `-apple-system`, `Segoe UI`, sans-serif.
- H1: `clamp(1.8rem, 2.8vw, 2.6rem)`, Zeilenhoehe 1.1.
- Abschnittstitel: etwa 1.1 rem; Score-Titel etwa 1.35 rem.
- Body/Form: etwa 0.92–0.98 rem mit 1.45–1.5 Zeilenhoehe.
- KPI-Wert: etwa 1.45 rem, bold; Zahlen verwenden tabellarische Ziffern (`.mono`).
- Tooltips/Metadaten: mindestens etwa 0.8 rem und hoher Kontrast; kritische Advice-Boundary-Information ist kein Tooltip-only-Inhalt.
- Waehrung, Prozent, Monat/Jahr und Quadratmeter bleiben am Wert sichtbar.

## Layout, Dichte und Responsive

Verifizierte Baseline:

- Wrapper: maximal 1320 px, 24 px Innenabstand.
- Desktop-Hauptgrid: 460 px Eingabespalte + flexible Ergebnisspalte, 22 px Gap.
- Wechsel auf eine Spalte bei 1080 px.
- Formularfelder: zwei Spalten, einspaltig unter 640 px.
- Score: 170 px Statusbereich + Text, einspaltig unter 700 px.
- KPI-Grid: 3 Spalten, 2 unter 980 px, 1 unter 620 px.
- Analyse: `1.15fr / .85fr`, einspaltig unter 980 px.
- Range-Cards: 4 Spalten, 2 unter 720 px.
- Standardradius: 18 px; Inputs/Buttons 12 px; Cards 16–18 px.

Regeln:

- Auf Desktop bleiben Annahmen und Ergebnis vergleichbar nebeneinander.
- Auf Mobile folgt zuerst die vollstaendige Eingabe, dann Score und Detailwerte; eine sticky Zusammenfassung darf keine Felder verdecken.
- Tabellen duerfen kontrolliert scrollen oder als Zeilen/Karten umbrechen; Header/Wertzuordnung bleibt sichtbar.
- Kein horizontales Seitenoverflow durch Tabelle, Tooltip oder Meter.
- Touchziele mindestens 44 × 44 px; der aktuelle 18-px-Info-Button ist deshalb als Implementierungsluecke zu behandeln, nicht als Zielstandard.

## Komponenten und Zustaende

### Formulare

- Jedes Feld besitzt dauerhaftes Label, Einheit und bei Bedarf kurze Hilfe.
- Fachlich zusammengehoerige Werte bleiben in nummerierten Abschnitten.
- Ziel fuer Invalid/fehlend: sichtbare Feldmeldung plus Fokus, keine stille NaN-/Nullrechnung. Die aktuelle `calc()`-Routine liest Werte direkt und nutzt HTML-`min`/`max` nicht als vollstaendiges Validierungsgate; das ist eine bekannte Runtime-Luecke und wird hier nicht kaschiert.
- Presets zeigen, welche Werte sie veraendern; sie sind Szenarien und keine Empfehlung.
- Primaeraktion `Deal pruefen`; Nebenaktionen bleiben visuell sekundaer.

### Tooltip

- Info-Button ist aktuell per Tastatur erreichbar und zeigt Hilfe auf Hover sowie Fokus. Ein eindeutiger zugaenglicher Name und programmatische Tooltip-Zuordnung fehlen noch.
- Tooltip enthaelt Erklaerung, aber keine alleinige rechtliche oder sicherheitskritische Information.
- Auf Touchgeraeten braucht Hilfe einen stabilen Tap-/Dismiss-Pfad; dieser ist im aktuellen Hover-/Focus-within-Muster nicht abschliessend nachgewiesen.

### Score und Deal-Meter

- Das Markup besitzt `Noch keine Berechnung`, startet aber direkt mit vorbelegtem Beispielszenario und `calc()`. Ein echter leerer Startzustand ist daher aktuell kein dauerhafter Runtime-State.
- Badge kombiniert Wort, Farbe und erklaerenden Text.
- Meter-Pointer hat textliche Entsprechung; Gradientenposition allein ist keine Aussage.
- Bewertungsmodus und zugrunde liegende Zielwerte werden in der Ergebnisnaehe sichtbar.

### KPIs, Tabelle und Einordnung

- KPI zeigt Label, Wert, Einheit und eine kurze Definition.
- Rechenuebersicht trennt Kaufnebenkosten, Invest, Darlehen, Miete, Zins, AfA und Steuerwirkung.
- Pill-Status (`good`/`warn`/`bad`) wird durch konkrete Analysezeile begruendet.
- Nicht unterstuetzte PLZ zeigt keinen geschaetzten Mietwert; manuelle Eingabe bleibt klar moeglich.
- Steuer- und Mieterhoehungshinweise bleiben als vereinfachte Orientierung markiert.

### Loading, Empty und Fehler

- Die lokale Berechnung braucht keinen kuenstlichen Loader; bei kuenftig asynchroner Quelle muss Progress + Text erscheinen.
- Empty unterscheidet `noch nicht gerechnet`, `nicht unterstuetzt` und `keine verwertbare Eingabe`.
- Fehler hinterlaesst keine teilweise aktualisierte Ergebnisflaeche.
- Ergebnis ist nach Korrektur reproduzierbar; alte Werte werden nicht als aktuelle Bewertung stehen gelassen.

## Accessibility und Motion

- Ziel: WCAG 2.2 AA.
- Vollstaendiger sichtbarer `:focus-visible`-Stil fuer Buttons, Inputs, Selects und Tooltip-Trigger ist Zielstandard; aktuell sind nur Input-/Select-`:focus` und Browserdefaults vorhanden.
- Labels sind programmatisch zugeordnet; eigene Feldfehlermeldungen und Tooltip-Beschreibungen noch nicht durchgehend.
- Status ist nicht farbexklusiv; Meter und Tabelle besitzen Textalternativen.
- Mindest-Touchziel 44 × 44 px, auch fuer Info-Trigger.
- `prefers-reduced-motion` soll Button-Transform, Tooltip-Fade und sonstige nicht notwendige Uebergaenge deaktivieren; ein entsprechender Media-Query fehlt aktuell.
- Zoom bis 200 % und 320-px-Breite duerfen keine Eingabe, Scoreerklaerung oder Advice Boundary verlieren.
- Dynamisch aktualisierte Ergebniszusammenfassung braucht eine angemessene Live-Region, ohne jede KPI einzeln vorzulesen; aktuell ist keine `aria-live`-Region vorhanden.

Die genannten Accessibility- und Validierungsluecken sind explizite Folgearbeit. Diese Spezifikationsaenderung veraendert weder UI noch Berechnungslogik.

## No-Gos

- Keine Kauf-, Rendite-, Steuer-, Miet- oder Rechtsgarantie.
- Kein `good` als automatisches Kaufsignal und kein `bad` als Ersatz fuer Analyse.
- Keine Zahl ohne Einheit, Zeitraum und erklaerbare Annahme.
- Keine automatische Mietschätzung fuer nicht belegte Orte.
- Keine Farbe-allein-Ampel, kein unbeschrifteter Meter und kein Tooltip-only-Disclaimer.
- Keine externen Fonts, Tracker, Frameworks oder Datenabfluesse ohne bewusste Produkt-/Datenschutzentscheidung.
- Kein visuelles Redesign, das Berechnungslogik, Thresholds oder Advice Boundary still veraendert.

## Agenten- und QA-Leitfaden

1. `DESIGN.md`, `PRODUCT.md`, `AGENTS.md`/`CLAUDE.md`, Single-File-Quelle und bei Formel-/Schwellwertarbeit den Fachskill lesen.
2. `design-agent` passend einsetzen; Wartung bleibt Konformitaetsarbeit, Redesign braucht ausdruecklichen Auftrag.
3. Visuellen Akzeptanzvertrag festhalten: Zielregion, Eingabe-/Ergebnisbezug, unveraenderte Formel/Schwelle, messbare Invariante und Invalid-/No-Estimate-Fallback.
4. Projektchecks und semantische Browser-QA bei 1440, 768 und 375 px ausfuehren; Tastatur, 200-%-Zoom und Reduce Motion pruefen.
5. Initialzustand, gueltige Rechnung, ungueltige Eingabe, nicht unterstuetzte PLZ, alle Bewertungsmodi, Tooltip-Fokus und lange Werte abnehmen.
6. Screenshots tatsaechlich ansehen und sichtbare Werte gegen DOM-/Berechnungsinvarianten pruefen. Ein Script-Pass ohne Zielregionbeweis ist kein Design-Pass.
7. Fachliche Aenderungen folgen separat den Quellen-/Testregeln; dauerhafte Designentscheidung wird hier synchronisiert.

## Pflege und Quellenhierarchie

`DESIGN.md` ist der Designvertrag. `immobilien-deal-checker.html` ist die Implementierungsquelle; Fachskill, Quellen und Tests bestimmen Formeln, Schwellen und Advice Boundary. Drift darf nicht optisch verdeckt werden: reale UI und Fachgrenze pruefen, Entscheidung dokumentieren und die betroffenen Quellen im selben Change angleichen.
