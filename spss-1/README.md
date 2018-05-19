# 720010 Computergestützte Datenauswertung I

## SPSS Praxis
### Umkodieren von Variablen
1. `Variablenansicht`
2. erste Spalte markieren
3. `Strg + F` (nach Variablenname suchen)
4. Wertebereich der Variable ansehen (wsl. 1-5)
5. `Transformieren` > `Umcodieren in dieselben Variablen` > `Alte und neue Werte` > Werte hinzufügen (1 auf 5; 2 auf 4; usw.) > `Weiter` > `Einfügen` (um Syntax-Fenster zu öffnen, dann **muss** dieser Befehl im Syntax-Fenster noch mit dem grünen Pfeil ausgeführt werden, ansonsten werden die Variablen nicht umkodiert ODER mit `OK` bestätigen und die Syntax aus dem Ausgabefenster kopieren) > *Syntax kopieren*


### Skala bilden
1. `Transformieren`
2. `Variable berechnen`
3. `Zielvariable` benennen > `Funktion` doppelklicken (z.B. `MEAN` befindet sich in Funktionsgruppe "Statistisch") > `Variablen` mit Doppelklick einfügen und Beistrich (Komma) trennen > *Numerischen Ausdruck* kopieren (für Variablenbeschriftung) > `OK`
4. Text aus Zwischenablage (*Numerischer Ausdruck*) in `Variablenansicht` in `Beschriftung` einfügen
5. Skala in `Variablenansicht` markieren > Icon "Tabelle mit µ (mü)" anklicken > `Ausgabefenster`
6. `Datenansicht` > Wert ablesen


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
2. zentrales Grenzwerttheorem (ab Gruppengröße 30)
   - Stichprobe größer als 30, da sich dann alles an die Normalverteilung annähert
3. grafisch
   - `Grafik` > `Diagrammerstellung` > `Histogramm` > `Normalverteilungskurve anzeigen` + `Anwenden` **!!!** > Variable auf X-Achse ziehen > `OK` > Interpretieren
4. Kolmogorow-Smirnow (kleine Stichproben) & Shapiro-Wilk (mittelgroße Stichproben)
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
- T-Test (*parametrisch*)
   - **Voraussetzung**: metrisch & normalverteilt
- Mann-Whitney-U-Test (*nicht parametrisch*)
   - **Voraussetzung**: falls eine der Voraussetzungen bei einer Variable von Pearson nicht zutrifft

#### (I) Voraussetzungen überprüfen und Fälle auswählen
1. [überprüfen ob die Variablen *metrisch* sind](#metrisch)
2. Variable und Ausprägungen notieren
3. `Daten` > `Fälle auswählen` > `Falls Bedingung zutrifft` > `Falls` > Variable doppelklicken + `=<Wert>` > `Weiter` > `OK` > in Datenansicht kontrollieren, dass einige der Werte durchgestrichen sind
4. [alle/beide Ausprägungen auf *Normalverteilung* überprüfen](#normalverteilt)

#### (II) Fälle zurücksetzen (alle Fälle)
**WICHTIG**: alle Fälle: `Daten` > `Fälle auswählen` > `Alle Fälle` > `OK`

#### (III) Test durchführen
##### T-Test (*parametrisch*)
1. `Analysieren` > `Mittelwerte vergleichen` > `T-Test bei unabhängigen Stichproben` > `Testvariable` in Feld *Testvariable(n)* ziehen > `Gruppierungsvariable` (z.B. Geschlecht) in *Gruppierungsvariable* ziehen > `Gruppen definieren` > Werte eintragen > `Weiter` > `OK`
2. Signifikanz beim Levene-Test der Varianzgleichheit
   - **gleich oder größer .05**: nicht signifikant = homogen/gleich 
   - **kleiner .05**: signifikant = nicht homogen/nicht gleich
3. Blick auf Signifikanz des T-Tests *Sig. (2-seitig)*
   - H0: es gibt *keinen signifikanten* Unterschied
     - Signifikanz **gleich oder größer .05**
   - H1: es gibt *einen signifikanten* Unterschied
     - Signifikanz **unter .05**
4. Teststatistik ist *T* + *Wert* (aus Tabelle ablesen)
  
##### Mann-Whitney-U-Test (*nicht parametrisch*)
1. `Analysieren` > `Nicht parametrische Tests` > `alte Dialogfelder` > `2 unabhängige Stichproben` > `Testvariable` in Feld *Testvariable(n)* ziehen > `Gruppierungsvariable` (z.B. Geschlecht) in *Gruppierungsvariable* ziehen > `Gruppen definieren` > Werte eintragen > `Weiter` > `OK`
2. Blick auf Signifikanz des Mann-Whitney-U-Test *Asymptotische Signifikanz (2-seitig)*
   - H0: es gibt *keinen signifikanten* Unterschied
     - Signifikanz **gleich oder größer .05**
   - H1: es gibt *einen signifikanten* Unterschied
     - Signifikanz **unter .05**
3. Teststatistik ist *U (Mann-Whitney-U)* + *Wert* (aus Tabelle ablesen)


### Unterschiedshypothese (abhängige Stichproben z.B. vorher/nachher)
#### 2 Arten von Tests
- T-Test (*parametrisch*)
   - **Voraussetzung**: metrisch & normalverteilt
- Wilcoxon-Test (*nicht parametrisch*)
   - **Voraussetzung**: falls eine der Voraussetzungen bei einer Variable von Pearson nicht zutrifft

#### (I) Voraussetzungen überprüfen
1. [überprüfen ob die Variablen *metrisch* sind](#metrisch)
2. [alle/beide Ausprägungen auf *Normalverteilung* überprüfen](#normalverteilt)

#### (II) Test durchführen
##### T-Test (*parametrisch*)
1. `Analysieren` > `Mittelwerte vergleichen` > `T-Test bei verbundenen Stichproben` > Variablen reinziehen > `OK`
2. Blick auf Signifikanz des *Tests bei gepaarten Stichproben* *Sig. (2-seitig)*
   - H0: es gibt *keinen signifikanten* Unterschied
     - Signifikanz **gleich oder größer .05**
   - H1: es gibt *einen signifikanten* Unterschied
     - Signifikanz **unter .05**
3. Teststatistik ist *T* + *Wert* (aus Tabelle ablesen)
  
##### Wilcoxon-Test (*nicht parametrisch*)
1. `Analysieren` > `Nicht parametrische Tests` > `alte Dialogfelder` > `2 verbundene Stichproben` > Variablen reinziehen > `OK`
2. Blick auf Signifikanz von *Statistik für Test* *Asymptotische Signifikanz (2-seitig)*
   - H0: es gibt *keinen signifikanten* Unterschied
     - Signifikanz **gleich oder größer .05**
   - H1: es gibt *einen signifikanten* Unterschied
     - Signifikanz **unter .05**
3. Teststatistik ist *Z* + *Wert* (aus Tabelle ablesen)


### Grafiken
- `Grafik` > `Diagrammerstellung` > passendes Diagramm auswählen


## Theorie
- Varianzheterogenität
   - TODO
