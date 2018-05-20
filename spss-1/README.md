# 720010 Computergestützte Datenauswertung I

## SPSS Praxis
### Umkodieren von Variablen
1. `Variablenansicht`
1. erste Spalte markieren
1. `Strg + F` (nach Variablenname suchen)
1. Wertebereich der Variable ansehen (wsl. 1-5)
1. `Transformieren` > `Umcodieren in dieselben Variablen` > `Alte und neue Werte` > Werte hinzufügen (1 auf 5; 2 auf 4; usw.) > `Weiter` > `Einfügen` (um Syntax-Fenster zu öffnen, dann **muss** dieser Befehl im Syntax-Fenster noch mit dem grünen Pfeil ausgeführt werden, ansonsten werden die Variablen nicht umkodiert ODER mit `OK` bestätigen und die Syntax aus dem Ausgabefenster kopieren) > *Syntax kopieren*


### Skala bilden
1. `Transformieren`
1. `Variable berechnen`
1. `Zielvariable` benennen > `Funktion` doppelklicken (z.B. `MEAN` befindet sich in Funktionsgruppe "Statistisch") > `Variablen` mit Doppelklick einfügen und Beistrich (Komma) trennen > *Numerischen Ausdruck* kopieren (für Variablenbeschriftung) > `OK`
1. Text aus Zwischenablage (*Numerischer Ausdruck*) in `Variablenansicht` in `Beschriftung` einfügen
1. Skala in `Variablenansicht` markieren > Icon "Tabelle mit µ (mü)" anklicken > `Ausgabefenster`
1. `Datenansicht` > Wert ablesen


### Zusammenhangshypothese
#### 2 Arten von Tests
- Pearson (*parametrisch*)
   - **Voraussetzung**: metrisch & normalverteilt
- Spearman (*nicht parametrisch*)
   - **Voraussetzung**: falls eine der Voraussetzungen bei einer Variable von Pearson nicht zutrifft

#### (I) Voraussetzungen überprüfen
##### *metrisch*?
1. für alle Variablen bei `Messniveau` in der `Variablenansicht` schauen, ob *metrisch* eingestellt ist

##### *normalverteilt*?
1. Kurtosis & Schiefe (nicht von der Gruppengröße abhängig)
   - `Analysieren` > `Deskriptive Statistiken` > `Deskriptive Statistik` > Variablen auswählen > `Optionen` > `Kurtosis` und `Schiefe` anhaken > `Weiter` > `OK`
   - Kurtosis und Schiefe müssen **zwischen** **-2** und **+2** liegen (Begründung: nach Andy Field)
1. zentrales Grenzwerttheorem (ab Gruppengröße 30)
   - Stichprobe größer als 30, da sich dann alles an die Normalverteilung annähert
1. grafisch
   - `Grafik` > `Diagrammerstellung` > `Histogramm` > `Normalverteilungskurve anzeigen` + `Anwenden` **!!!** > Variable auf X-Achse ziehen > `OK` > Interpretieren
1. Kolmogorow-Smirnow (kleine Stichproben) & Shapiro-Wilk (mittelgroße Stichproben)
   - `Analysieren` > `Deskriptive Statistiken` > `Explorative Datenanalyse` > Variable in *Abhängige Variablen* ziehen > `Diagramme` > `Normalverteilungsdiagramm mit Tests` anhaken > `Weiter` > `OK`
   - zwei Hypothesen
     - H0: unterscheiden sich *nicht signifikant* von der Normalverteilung
       - Signifikanz **gleich oder größer .05**
     - H1: unterscheiden sich *signifikant* von der Normalverteilung
       - Signifikanz **unter .05**

#### (II) Test durchführen (Pearson & Spearman)
- `Analysieren` > `Korrelation` > `Bivariat` > Variablen auswählen > `Korrelationskoeffizient` festlegen: Pearson oder Spearman (immer zweiseitig)
  - H0: es gibt *keinen signifikanten* Zusammenhang
    - Signifikanz **gleich oder größer .05**
  - H1: es gibt *einen signifikanten* Zusammenhang
    - Signifikanz **unter .05**


### Unterschiedshypothese (unabhängige Stichproben z.B. Männer/Frauen)
#### 2 Arten von Tests
- *t*-Test (*parametrisch*)
   - **Voraussetzung**: metrisch & normalverteilt
- Mann-Whitney-U-Test (*nicht parametrisch*)
   - **Voraussetzung**: falls eine der Voraussetzungen bei einer Variable von Pearson nicht zutrifft

#### (I) Voraussetzungen überprüfen und Fälle auswählen
1. [überprüfen ob die Variablen *metrisch* sind](#metrisch)
1. Variable und Ausprägungen notieren
1. `Daten` > `Fälle auswählen` > `Falls Bedingung zutrifft` > `Falls` > Variable doppelklicken + `=<Wert>` > `Weiter` > `OK` > in Datenansicht kontrollieren, dass einige der Werte durchgestrichen sind
1. [alle/beide Ausprägungen auf *Normalverteilung* überprüfen](#normalverteilt)

#### (II) Fälle zurücksetzen (alle Fälle)
**WICHTIG**: alle Fälle: `Daten` > `Fälle auswählen` > `Alle Fälle` > `OK`

#### (III) Test durchführen
##### *t*-Test (*parametrisch*)
1. `Analysieren` > `Mittelwerte vergleichen` > `T-Test bei unabhängigen Stichproben` > `Testvariable` in Feld *Testvariable(n)* ziehen > `Gruppierungsvariable` (z.B. Geschlecht) in *Gruppierungsvariable* ziehen > `Gruppen definieren` > Werte eintragen > `Weiter` > `OK`
1. Signifikanz beim Levene-Test der Varianzgleichheit
   - **gleich oder größer .05**: nicht signifikant = homogen/gleich 
   - **kleiner .05**: signifikant = nicht homogen/nicht gleich
1. Blick auf Signifikanz des *t*-Tests *Sig. (2-seitig)*
   - H0: es gibt *keinen signifikanten* Unterschied
     - Signifikanz **gleich oder größer .05**
   - H1: es gibt *einen signifikanten* Unterschied
     - Signifikanz **unter .05**
1. Teststatistik ist *T* + *Wert* (aus Tabelle ablesen)
  
##### Mann-Whitney-U-Test (*nicht parametrisch*)
1. `Analysieren` > `Nicht parametrische Tests` > `alte Dialogfelder` > `2 unabhängige Stichproben` > `Testvariable` in Feld *Testvariable(n)* ziehen > `Gruppierungsvariable` (z.B. Geschlecht) in *Gruppierungsvariable* ziehen > `Gruppen definieren` > Werte eintragen > `Weiter` > `OK`
1. Blick auf Signifikanz des Mann-Whitney-U-Test *Asymptotische Signifikanz (2-seitig)*
   - H0: es gibt *keinen signifikanten* Unterschied
     - Signifikanz **gleich oder größer .05**
   - H1: es gibt *einen signifikanten* Unterschied
     - Signifikanz **unter .05**
1. Teststatistik ist *U (Mann-Whitney-U)* + *Wert* (aus Tabelle ablesen)


### Unterschiedshypothese (abhängige Stichproben z.B. vorher/nachher)
#### 2 Arten von Tests
- T-Test (*parametrisch*)
   - **Voraussetzung**: metrisch & normalverteilt
- Wilcoxon-Test (*nicht parametrisch*)
   - **Voraussetzung**: falls eine der Voraussetzungen bei einer Variable von Pearson nicht zutrifft

#### (I) Voraussetzungen überprüfen
1. [überprüfen ob die Variablen *metrisch* sind](#metrisch)
1. [alle/beide Ausprägungen auf *Normalverteilung* überprüfen](#normalverteilt)

#### (II) Test durchführen
##### T-Test (*parametrisch*)
1. `Analysieren` > `Mittelwerte vergleichen` > `T-Test bei verbundenen Stichproben` > Variablen reinziehen > `OK`
1. Blick auf Signifikanz des *Tests bei gepaarten Stichproben* *Sig. (2-seitig)*
   - H0: es gibt *keinen signifikanten* Unterschied
     - Signifikanz **gleich oder größer .05**
   - H1: es gibt *einen signifikanten* Unterschied
     - Signifikanz **unter .05**
1. Teststatistik ist *T* + *Wert* (aus Tabelle ablesen)
  
##### Wilcoxon-Test (*nicht parametrisch*)
1. `Analysieren` > `Nicht parametrische Tests` > `alte Dialogfelder` > `2 verbundene Stichproben` > Variablen reinziehen > `OK`
1. Blick auf Signifikanz von *Statistik für Test* *Asymptotische Signifikanz (2-seitig)*
   - H0: es gibt *keinen signifikanten* Unterschied
     - Signifikanz **gleich oder größer .05**
   - H1: es gibt *einen signifikanten* Unterschied
     - Signifikanz **unter .05**
1. Teststatistik ist *Z* + *Wert* (aus Tabelle ablesen)


### Grafiken
- `Grafik` > `Diagrammerstellung` > passendes Diagramm auswählen


## Theorie
1. Was bedeutet Signifikant und welche Signifikanzniveaus gelten in der Psychologie als Grenzwerte? [1](https://www.spektrum.de/lexikon/psychologie/signifikanzniveau/14251)
   - Niveau des Alpha-Fehlers (Fehler erster Art), d.h. des Fehlers, eine Nullhypothese abzulehnen, obwohl sie richtig ist
   - per Konvention festgelegte Höchstgrenzen
     - **< 5%** (signifikant, \*)
     - **< 1%** (sehr signifikant, \*\*)
     - **< 0,1%** (hoch signifikant, \*\*\*)
1.	Was bedeutet Normalverteilung und wie kann man diese überprüfen?
   - Verteilungsfunktion nach Gauß die besagt, dass ab einer gewissen Stichprobengröße (zentraler Grenwertsatz: 30) zufallsbasierte Daten immer annähernd normalverteilt sind
   - sprich es gibt den Erwartungswert μ und die Standardabweichung σ, die die Daten in form einer Glockenkurve beschreiben
   - Möglichkeiten zu überprüfen ob Daten normalverteilt sind
     - Kurtosis & Schiefe
     - grafisches Begutachten
     - Kolmogorow-Smirnow (kleine Stichproben)
     - Shapiro-Wilk (mittelgroße Stichproben)
1.	Was kann man in einem Streudiagramm gut sehen?
   - Zusammenhänge zwischen den Daten (z.B. linear, quadratisch, kubisch, ...)
1.	Was kann man in einem Boxplot besonders gut ablesen?
   - Ein Box-Plot soll schnell einen Eindruck darüber vermitteln, in welchem Bereich die Daten liegen und wie sie sich über diesen Bereich verteilen.
   - Fünf-Punkte-Zusammenfassung: Median, zwei Quartile und die beiden Extremwerte 
1.	Was bedeutet Varianzhomogenität?
  - = *Homoskedastizität*
  - die Werte in den einzelnen Gruppen weisen die gleiche Varianz auf
  - wird vom *t*-Test für unabhängige Gruppen vorausgesetzt
  - wird mit Levene-Test überprüft
1.	Was bedeutet Varianzheterogenität?
  - = *Heteroskedastizität*
  - die Werte in den einzelnen Gruppen weisen unterschiedliche Varianzen auf
  - wird mit Levene-Test überprüft
1.	Was ist ein Outliner und welchen Einfluss haben Outliner auf Daten?
   - Wert der sehr stark vom Erwartungswert abweicht (zu Deutsch *Ausreißer* genannt)
   - sie verzerren z.B. das arithmetische Mittel sehr stark
   - prüfen ob es sich um Messfehler handelt
1.	Welche Maße der zentralen Tendenz gibt es und was bedeuten diese?
   - **Mittelwert**: arithmetisches Mittel (Summe/Anzahl; wird von Ausreißern stark beeinflusst)
   - **Median**: Zentralwert, Wert der in der Mitte einer sortierten Reihe liegt (unsensibel gegenüber Ausreißern)
   - **Modus**: häufigster Wert
