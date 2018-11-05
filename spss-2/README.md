# 720010 Computergestützte Datenauswertung I

## SPSS Praxis
### Faktorenanalyse
Korrelation zw. 2 Variablen: *Kausalität*, *3. Variable*
Konstrukte (Notation: Oval) können durch Variablen (Notation: Rechteck) beobachtet werden
Das Konstrukt (z.b. Ängstlichkeit, Neurotizismus), existiert nur in unserer Theorie

Analysieren -> Dimensionsreduktion -> Faktorenanalyse -> Variablen auswählen -> Deskriptive Statistik "KMO und Bartlett-Test auf Sphärizität" -> Extraktion "Hauptachsen-Faktorenanalyse" + Screeplot -> Rotation "Varimax" -> Optionen "Sortiert nach Größe"

Analysieren -> Dimensionsreduktion -> Faktorenanalyse -> Variablen auswählen -> Deskriptive Statistik "KMO und Bartlett-Test auf Sphärizität" -> Extraktion "Hauptachsen-Faktorenanalyse" + Screeplot -> Rotation "Varimax" -> Optionen "Sortiert nach Größe" + "Kleine Koeffizienten unterdrücken, Absolutwert unter ,30"

Es verbergen sich so viele Konstrukte hinter den Faktoren, wie die deren Eigenwert > 1


# 1. Übungsblatt

## Aufgabe 1 (TS_Sinnkrise)
Analysieren -> Skala -> Reliabilitätsanalyse | Statistiken (Skala wenn Item gelöscht + Korrelationen) -> Ok

### Lösung
- Cronbach's Alpha: ,908
- Trennschärfen: Korrigierte Item-Skala-Korrelation (mind. ,5)
- SMC: Quadrierte Multiple Korrelation (mind. ,25)

## Aufgabe 2
umkodieren

## Aufgabe 3
- Transformieren -> Variable berechnen -> TS_Sinnkrise (`MEAN(<variable[0]>,<variable[1]>,...`)
- Analysieren -> Deskriptive Statistiken -> Explorative Datenanalyse -> ...
- Kolmogorov-Smirnov
  - Frau D(173) = 0,210; p < .001
  - Mann D(82) = 0,176; p < .001
- Levene-Test
  - F(1, 253) = 8,426; p = .004
- T-Test für unabhängige Stichproben
  - Frau Mittelwert: 1,7988; Standardabweichung: ,98960
  - Mann Mittelwert: 2,2073; Standardabweichung: 1,20265
  
## Aufgabe 4
- KS
  - Frau: D(173) = ,142; p = ,000
  - Mann: D(82) = ,081; p = ,200
- Levene
  - F(1, 253) = 3,582; p = ,060 (,05 is die Grenze für Signifikanz)
- Ergebnis: t(df)=T; p=Sig
