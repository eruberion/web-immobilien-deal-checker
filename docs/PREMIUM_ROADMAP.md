# Historischer Premium-Entwurf – web-immobilien-deal-checker

> Stand: 15. April 2026
> Status: **Nicht freigegebene Arbeitshypothese.** Dieses Dokument ist weder
> eine aktuelle Preisentscheidung noch ein Umsetzungsauftrag. Vor einer
> Aktivierung müssen Marktvalidierung, Produktfreigabe, Advice-Boundary,
> Zahlungs-/Datenschutzfluss und aktuelle Preisannahmen erneut geprüft werden.

## Historische Monetarisierungshypothese

- **Hauptmodell:** Freemium + **Monatsabo + Jahresabo**
- **Kein Lifetime** am Anfang
- Monatsabo ist hier wichtiger als bei den anderen Projekten, weil die Nutzung oft suchphasengetrieben ist

## Historische Preisannahmen

- damalige Arbeitshypothese: **59,99 € / Jahr**
- **Monatsabo:** **9,99 bis 12,99 €**

## Warum dieses Modell

- Immobilien-Tools könnten einen hohen Orientierungsnutzen und eine relevante
  Zahlungsbereitschaft erreichen; beides ist für dieses Projekt noch nicht
  belastbar validiert.
- Gleichzeitig ist die Nutzung oft phasenweise intensiv statt dauerhaft.
- Deshalb funktionieren Monatsabo und Jahresabo hier besser als ein reiner Einmalkauf.

## Zielbild Free vs Premium

### Free

- Schnelle Einmal-Pruefung eines Deals
- Kernkennzahlen
- Einfache Annahmen
- Kein Speichern, kein Export, kein Vergleich

### Premium

- Gespeicherte Deals
- Deal-Vergleich
- Szenario- und Sensitivitaetsanalyse
- Erweiterte Annahmen fuer Miete, Leerstand, Ruecklagen, Finanzierung
- Export / PDF
- Spaeter: regionale Presets und Portfolio-Sicht

## Frühere, nicht freigegebene Umsetzungsreihenfolge

1. **Save / Compare / Export als Premium-Kern bauen**
2. **Monatsabo prominent mit Jahresabo daneben anbieten**
3. **Nach erstem Ergebnis paywallen, nicht vorher**
4. **Jahresabo mit klarem Rabatt gegenueber Monatsabo kommunizieren**
5. **Lifetime erst pruefen, wenn das Produkt bewusst klein bleiben soll**

## Offene Produktentscheidung

- Paket, Preis, Abrechnungsmodell und Paywall-Zeitpunkt sind nicht entschieden.
- Die früheren Werte `59,99 € / Jahr` und `9,99 bis 12,99 € / Monat` dürfen
  ohne neue Validierung nicht in Produkt, Marketing oder Checkout übernommen
  werden.
