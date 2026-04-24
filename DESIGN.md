# DESIGN.md — Immobilien Deal Checker

## Zweck
Dieses Dokument beschreibt die visuelle Richtung des Immobilien Deal Checkers, damit das Produkt schnell, ehrlich und nützlich bleibt — ohne unnötige Tool-Spielerei oder optische Überladung.

Abgeleitet aus:
- `README.md`
- `immobilien-deal-checker.html`
- `docs/PREMIUM_ROADMAP.md`
- vorhandenen Web-/Design-Skills im Repo

## Produktcharakter
Der Immobilien Deal Checker ist ein schneller Plausibilitätsrechner für Kapitalanlage-Immobilien.
Die Kernwirkung soll sein:
- direkt verständlich
- effizient
- glaubwürdig
- pragmatisch
- fokussiert auf Nutzen statt Show

## Zielbild
**Souveränes Analyse-Tool statt hübscher Immobilien-Marketing-Skin.**

Das Produkt darf modern wirken, aber muss zuerst klar und rechnerisch belastbar erscheinen.

## Visuelle Richtung

### Bildsprache
- dunkle, sachliche Tool-Oberfläche
- klare Paneele und Eingabeblöcke
- starke Lesbarkeit
- semantische Farbgebung für Bewertung
- wenig dekorative Elemente

### Stimmung
- ehrlich
- direkt
- analytisch
- ruhig
- nicht protzig

## Designprinzipien

### 1. Geschwindigkeit schlägt Dekoration
Der Nutzer will schnell eingeben, schnell verstehen, schnell entscheiden.

Deshalb:
- kurze Wege
- klare Formularstruktur
- direkte Ergebnisse
- wenig visuelle Ablenkung

### 2. Bewertung muss glaubwürdig wirken
Wenn Score, Deal-Meter und KPI-Flächen zu verspielt aussehen, leidet Vertrauen.

Deshalb:
- einfache, robuste Visualisierung
- klare Statusfarben
- zurückhaltende Akzente
- nachvollziehbare Einordnung

### 3. Hilfen sollen entlasten, nicht nerven
Tooltips, Hinweise und Erklärungstexte sind wichtig, dürfen aber nicht den Flow blockieren.

### 4. Gute Dichte statt Leerflächen-Luxus
Im Gegensatz zu Premium-Marketingseiten darf dieses Produkt dichter sein.
Aber: dichte UI ist nicht gleich chaotische UI.

## Komponenten-Richtung

### Formularbereiche
- logisch gruppiert
- klare Abschnittsüberschriften
- Eingaben sachlich und robust
- Hilfetexte klein, aber gut lesbar

### Ergebnisse
- Deal-Score prominent
- KPI-Blöcke einheitlich
- Bewertung logisch von oben nach unten lesbar
- Analyse und Tabelle nicht gegeneinander konkurrieren lassen

### Statusfarben
- Grün = gut
- Orange = prüfen
- Rot = kritisch
- Blau nur als neutraler Akzent, nicht als semantischer Bewertungsersatz

## Animation / Motion
Für dieses Projekt ist `motion` **nicht priorisiert**.

Wenn es überhaupt eingesetzt wird, dann nur für:
- dezente Section-Reveals
- kleine Zustandswechsel
- sanftes Ein-/Ausblenden von Hilfeblöcken

Nicht sinnvoll sind:
- große Hero-Animationen
- spielerische Card-Moves
- dynamische Scroll-Effekte

Regel: Dieses Produkt gewinnt mehr durch Klarheit als durch Animation.

## Do / Don't

### Do
- schnelle Bedienbarkeit priorisieren
- Ergebnis-Logik klar staffeln
- Toolcharakter sichtbar lassen
- semantische Farben diszipliniert einsetzen
- Inputs, KPIs und Auswertung visuell vereinheitlichen

### Don't
- Immobilienmarketing-Look
- zu viele Glows oder Gradients
- spielerische Bewegung
- visuell zu weiche, unpräzise Ergebnisdarstellung
- dekorative Überladung

## Naheliegende Umsetzungshebel
- Eingabeblöcke noch konsequenter vereinheitlichen
- KPI- und Analysebereiche stärker auf Scanbarkeit trimmen
- Score-/Meter-Bereich noch klarer priorisieren
- mobile Eingabe-UX weiter verbessern
- ggf. später leichte visuelle Veredelung ohne Verlust an Tool-Klarheit
