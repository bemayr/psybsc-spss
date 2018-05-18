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




## Theorie
- Varianzheterogenität
  - ???
