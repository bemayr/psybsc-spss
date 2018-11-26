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


# 2. Übungsblatt

## Aufgabe 1
*nicht Prüfungsstoff*: Unterschiedshypothese, dann T-Test oder Welch-Test machen
F(<Gruppenanzahl> - 1, <n> - 2)

## Aufgabe 2
> Analysieren -> nicht parametrische Tests -> klassische Dialogfelder -> 2 unabhängige Stickproben

*ähnlich zu Aufgabe 1, aber es können Ausreißer auftreten und unsere Statistik verzerren*: daher kein T-Test oder Welch-Test, sondern **U-Test**, oder **Mann-Whitney-Test** (runterbrechen auf Ordinalskalenniveau, Rangtransformation)

Gruppierungsvariable: Neurotizismus_dichotom (+ Gruppen definieren)
Testvariablen: Zugehörigkeit

Deskriptive Statistik ist beim U-Test der mittlere Rang pro Gruppe
gering neurotizistisch: 95,12
hoch neurotizistisch: 74,51

Inferenzstatistischer Test: U-Test: 2698,5; p = ,006

## Aufgabe 3
> Analysieren -> Mittelwerte vergleichen -> Einfaktorielle Varianzanalyse
> *Post-Hoc:* GT2 nach Hochberg + Games-Howell
> *Optionen:* Deskriptive Statistik + Test auf Homogenität der Varianzen + Welch

*Faktor:* Charaktertyp
*Abhängige Variablen:* TS_Sinnerfülltheit

**Deskriptive Statistik:** *Mittelwerte* und *Standardabweichung* der einzelnen Gruppen
Sanguiniker: 4,4080   1,05053
Phlegmatiker: 3,5389   1,02296
Choleriker: 3,5846   ,76926
Melancholiker: 3,0351   ,74174

F(<df1>,<df2>)=<Levene-Statistik>; p=<Signifikanz> **=>** F(3,165)=2,042; p=,110
Man kann die Voraussetzung als gegeben annehmen, dass die Varianzen in den Gruppen homogen sind, da der Levene-Test nicht signifikant ist. (p > ,05), also wird obere Box berichtet, sonst untere Box.
F(3,165) = 20,493; p = ,000 (oder p < ,001)
                                           
Wenn Levene-Test nicht signifikant (also Varianzhomogenität gegeben), dann nehmen wir GT2 (Hochberg), dann p berichten
Sanguiniker|Phlegmatiker: ,000
Sanguiniker|Choleriker: ,001
Sanguiniker|Melancholiker: ,000
Phlegmatiker|Choleriker: 1,000
Phlegmatiker|Melancholiker: ,059
Choleriker|Melancholiker: ,067

> Bei der Prüfung geht es nur darum, dass ihr die Zahlen richtig abschreiben könnt. - Daniel Purtscheller, 19.11.2018

## Aufgabe 4
> Analysieren -> nicht parametrische Tests -> unabhängige Stichproben
> *Einstellungen:* Tests anpassen -> Einfaktorielle ANOVA nack Kruskal-Wallis + Mehrfahvergleiche "alle paarweise"
> *Ausgabefenster:* Hypothesentestübersicht

*ähnlich zu Aufgabe 3, aber Rangtransformation*:

*Gruppierungsvariable:* Charaktertyp, *Testvariable:* Bedeutsamkeit

Ansicht: Paarweise Vergleiche von Charaktertyp
Deskriptive Statistik (aus Grafik ablesen), mittlere Ränge:
Sanguiniker: 117,83
Phlegmatiker: 88,24
Choleriker: 74,62
Melancholiker: 58,89

Inferenzstatistischer Test:
H(3,169) = 40,341; p = ,000 (asymptotische Signifikanz, 2-seitiger Test)

Überschreitungswahrscheinlichkeiten
Melancholiker|Choleriker: 1,000
Melancholiker|Phlegmatiker: ,028
Melancholiker|Sanguiniker: ,000
Choleriker|Phlegmatiker: 1,000
Choleriker|Sanguiniker: ,001
Phlegmatiker|Sanguiniker: ,033

## Aufgabe 5
gleich wie 3, nur da Signifikanz vom Levene-Test < ,05 ist, Welch-Test (also untere Box) nehmen

"Das ist einfach ein mathematischer Firlefanz, und das ist einfach eine Korrektur" - Daniel Purtscheller, 19.11.2018

dann auch die untere Hälfte (Games-Howell) interpretieren

## Aufgabe 6
> Analysieren -> Allgemeines lineares Modell -> Univariat
> *Optionen:* Deskriptive Statistik

Deskriptive Statistiken
Vier Ausprägungen: Mittelwert + Standardabweichung aufschreiben

"Hier wo das Sternchen für Multiplizieren ist, das ist der Interaktionseffekt."
F(1,165) = 4,216; p = ,042
165 aus Fehler ablesen

## Aufgabe 7
F(1,165) = ,003; p = ,960
