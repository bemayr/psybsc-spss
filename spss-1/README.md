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

#### 2 Arten
##### Pearson
**Voraussetzung**: metrisch & normalverteilt
##### Spearman
falls eine der Voraussetzungen bei einer Variable von Pearson nicht zutrifft

### auf *metrisch* überprüfen
bei `Messniveau` in der `Variablenansicht` schauen, ob das *metrisch* ist

### *Normalverteilung* überprüfen
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

#### Pearson & Spearman
- `Analysieren` > `Korrelation` > `Bivariat` > Variablen auswählen > `Korrelationskoeffizient` festlegen: Pearson oder Spearman (immer zweiseitig)
  - H0: es gibt *keinen signifikanten* Zusammenhang
    - Signifikanz **gleich oder größer .05**
  - H1: es gibt *einen signifikanten* Zusammenhang
    - Signifikanz **unter .05**


### Unterschiedshypothese (unabhängige Stichproben)
#### Fälle auswählen
- metrisch überprüfen (TODO: Link)
- Variable und Ausprägungen notieren
- `Daten` > `Fälle auswählen` > `Falls Bedingung zutrifft` > `Falls` > Variable doppelklicken + `=<Wert>` > `Weiter` > `OK` > in Datenansicht kontrollieren, dass einige der Werte durchgestrichen sind
- auf Normalverteilung überprüfen (TODO: Link) für alle/beide Ausprägungen durchführen

**WICHTIG**: alle Fälle: `Daten` > `Fälle auswählen` > `Alle Fälle` > `OK`

##### 2 Fälle
###### parametrisch (metrisch + normalverteilt)
- T-Test
   - `Analysieren` > `Mittelwerte vergleichen` > `T-Test bei unabhängigen Stichproben` > `Testvariable` in Feld *Testvariable(n)* ziehen > `Gruppierungsvariable` (z.B. Geschlecht) in *Gruppierungsvariable* ziehen > `Gruppen definieren` > Werte eintragen > `Weiter` > `OK`
  - Signifikanz beim Levene-Test der Varianzgleichheit
    - >=.05 nicht signifikant - homogen/gleich 
    - <.05 signifikant - nicht homogen/nicht gleich
  - Blick auf Signifikanz des T-Tests *Sig. (2-seitig)*
     - H0: es gibt *keinen signifikanten* Unterschied
       - Signifikanz **gleich oder größer .05**
     - H1: es gibt *einen signifikanten* Unterschied
       - Signifikanz **unter .05**
  - Teststatistik ist *T* + *Wert* (aus Tabelle ablesen)
  

###### nicht parametrisch (Bedingung verletzt)


## Theorie
- Varianzheterogenität
  - ???
