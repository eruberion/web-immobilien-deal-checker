---
name: immobilien-deal-expert
description: Fach- und Produktregeln fuer den deutschen Immobilien-Deal-Checker. Immer verwenden bei Kaufpreis-, Finanzierungs-, Cashflow-, Rendite-, Tilgungs-, Restschuld-, AfA-, Steuer-, Miet-, Leerstands-, Instandhaltungs- oder Verkaufsszenarien sowie zugehoerigen Fachtexten und Reports. Verlangt nachvollziehbare Modellrechnungen, offizielle Quellen und eine klare Advice-Boundary.
---

# Immobilien-Deal-Expert

## Prioritaeten

1. Rechenlogik und Einheiten fachlich konsistent halten.
2. Annahmen, Stichtag und Modellgrenzen am Ergebnis sichtbar machen.
3. Personen- und Objektdaten lokal und sparsam verarbeiten.
4. Optimistische, Basis- und Stressszenarien vergleichbar darstellen.

## Produktgrenze

Der Deal-Checker ist ein orientierendes Planungswerkzeug, keine Steuer-, Rechts-,
Finanzierungs-, Anlage- oder Kaufberatung. Keine individuelle Empfehlung und
keine Garantie fuer Rendite, Finanzierbarkeit, Steuerwirkung oder Wertentwicklung
formulieren. Ergebnisse als Modellrechnung kennzeichnen.

## Quellenworkflow

Vor Aenderungen an Konstanten oder Fachtexten Repo-Dokumentation und Tests lesen.
Zeitvariable Werte nicht in diesem Skill festschreiben. Fuer Rechts- und
Steuerparameter primaer amtliche Quellen verwenden, insbesondere Gesetze im
Internet, Bundesgesetzblatt, BMF, Landesfinanzverwaltungen, Destatis und
Gutachterausschuesse. Stichtag, Gueltigkeitszeitraum, Quelle und Vereinfachung
gemeinsam dokumentieren.

## Modellregeln

- Kaufnebenkosten nach Bundesland und Eingabejahr getrennt vom Kaufpreis halten.
- Gebaeude- und Bodenanteil nicht vermischen; AfA nur auf die fachlich zulaessige
  Bemessungsgrundlage anwenden.
- Eigenkapital, Darlehen, Zins, Anfangstilgung, Sondertilgung, Rate, Zinsbindung
  und Restschuld in derselben Zahlungslogik berechnen.
- Zahlungszeitpunkte explizit festlegen; Monats- und Jahreswerte nicht still
  mischen.
- Kaltmiete, nicht umlagefaehige Kosten, Verwaltung, Instandhaltung, Leerstand,
  Mietausfall und CapEx separat modellieren.
- Brutto- und Nettorendite, Eigenkapitalrendite, Cashflow und Vermoegenszuwachs
  nicht als austauschbare Kennzahlen behandeln.
- Steuerwirkungen nur mit sichtbaren Annahmen und ohne scheinexakte individuelle
  Steuerprognose darstellen.
- Wertsteigerung, Mietentwicklung und Anschlusszins in Stressszenarien testen;
  nominale und reale Werte eindeutig beschriften.
- Verkaufsszenarien mit Haltedauer, Restschuld, Transaktionskosten und moeglichen
  Steuern rechnen; keine Steuerfreiheit pauschal behaupten.

## Konsistenz und Tests

Berechnungen zentral halten und nicht in UI-Komponenten duplizieren. Jede
fachliche Aenderung braucht Unit-, Grenzwert- und Regressionsfaelle, darunter
Nullwerte, negative Cashflows, hohe Leerstaende, Zinswechsel und Rundungen.
Summen aus Report, Detailansicht und Vergleich muessen dieselbe Engine verwenden.

## Datenschutz und Darstellung

- Eingaben als schutzbeduerftige Finanz- und Vermoegensdaten behandeln.
- Keine Nutzerdaten oder Berechnungsergebnisse in Telemetrie oder Logs schreiben.
- Local-first nicht mit Schutz vor XSS, Malware oder gemeinsam genutzten Geraeten
  gleichsetzen.
- Importierte oder persistierte Daten an der Vertrauensgrenze validieren.
- Ergebnisse, Warnungen, Annahmen und Quellen barrierearm und ohne reine
  Farbcodierung darstellen.

Bei Auth, Sync, Backend, Datenbank, Verschluesselung, Zahlung oder Deployment
zusaetzlich einen passenden Security-Skill laden. Bei unklarer fachlicher
Grundlage stoppen, offene Annahme benennen und eine belastbare Quelle verlangen.
