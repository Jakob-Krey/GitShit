# Deskriptive und Explorative beschreibung "Ecommerce Customer Churn"


## [Über Den Datensatz](#der-datensatz)
##  [Aufarbeiteung des Datensatzes](#daten-aufarbeiten)
### [Normalisieren von Variablen](#werte-der-variablen-auf-ein-skalenniveau-bringen-normalisieren)
##  [Der Aufgearbeitete Datensatz](#aufgearbeiteter-datensatz)

# Der Datensatz

### Datenquelle
https://www.kaggle.com/datasets/ankitverma2010/ecommerce-customer-churn-analysis-and-prediction


## Beschreibung der Variablen:
- ***CustomerID*** 
<br>Datentyp: ***int64*** 
<br>Bedeutung: Dies ist eine eindeutige Kennung oder Identifikationsnummer für jeden Kunden 
<br>Interpretation:
- ***Churn*** 
<br>Datentyp: ***int64*** 
<br>Bedeutung: Dies ist eine binäre Variable, die angibt, ob ein Kunde abgewandert ist oder nicht. 
<br>Interpretation: 1 = ja ; 0 = nein
<br>einzigartige Werte: [1 0]
- ***Tenure*** 
<br>Datentyp: ***float64*** 
<br>Bedeutung: Dies ist die Dauer oder Zeitspanne, die ein Kunde bereits Kunde ist 
<br>Interpretation: Dauer in Monaten
<br>einzigartige Werte: [ 4 10  0 13 11  9 19 20 14  8 18  5  2 30  1 23  3 29  6 26 28  7 24 25
 15 22 27 16 12 21 17 50 60 31 51 61]
- ***PreferredLoginDevice*** 
<br>Datentyp: ***object*** 
<br>Bedeutung: Dies gibt an, welches Gerät der Kunde bevorzugt, um sich bei seinem Konto anzumelden
<br>Interpretation:
<br>einzigartige Werte: ['Mobile Phone' 'Phone' 'Computer']
- ***CityTier*** 
<br>Datentyp: ***int64*** 
<br>Bedeutung: Dies ist eine Kategorisierung der Stadt, in der der Kunde lebt <br>Interpretation: Es könnte 1 für Großstädte, 2 für mittelgroße Städte und 3 für kleine Städte stehen.
<br>einzigartige Werte: [3 1 2]
- ***WarehouseToHome*** 
<br>Datentyp: ***float64*** 
<br>Bedeutung: Die durchschnittliche Entfernung zum Wohnort des Kunden
<br>Interpretation: Entfernung In Kilometern
<br>einzigartige Werte: [  6.   8.  30.  15.  12.  22.  11.   9.  31.  18.  13.  20.  29.  28.
  26.  14.  nan  10.  27.  17.  23.  33.  19.  35.  24.  16.  25.  32.
  34.   5.  21. 126.   7.  36. 127.]
- ***PreferredPaymentMode*** 
<br>Datentyp: ***object*** 
<br>Bedeutung: Dies gibt die bevorzugte Zahlungsmethode des Kunden an
<br>Interpretation:
<br>einzigartige Werte: ['Debit Card' 'UPI' 'CC' 'Cash on Delivery' 'E wallet' 'COD' 'Credit Card']
- ***Gender*** 
<br>Datentyp: ***object*** 
<br>Bedeutung: Das Geschlecht des Kunden
<br>Interpretation:
<br>einzigartige Werte: ['Female' 'Male']
- ***HourSpendOnApp*** 
<br>Datentyp: ***float64*** 
<br>Bedeutung: Die durchschnittliche Zeit, die der Kunde täglich auf der Unternehmens-App verbringt
<br>Interpretation:
<br>einzigartige Werte: [3. 2. 2.93153488 1. 0. 4. 5.]
- ***NumberOfDeviceRegistered*** 
<br>Datentyp: ***int64*** 
<br>Bedeutung:  Die Anzahl der Geräte, die der Kunde bei dem Unternehmen registriert hat.
<br>Interpretation:
<br>einzigartige Werte: [3 4 5 2 1 6]
- ***PreferedOrderCat*** 
<br>Datentyp: ***object*** 
<br>Bedeutung: Die bevorzugte Kategorie von Produkten oder Dienstleistungen, die der Kunde bestellt
<br>Interpretation:
<br>einzigartige Werte: ['Laptop & Accessory' 'Mobile' 'Mobile Phone' 'Others' 'Fashion' 'Grocery']
- ***SatisfactionScore*** 
<br>Datentyp: ***int64*** 
<br>Bedeutung: Dies ist eine Bewertung die die Zufriedenheit des Kunden wiederspiegelt
<br>Interpretation:
<br>einzigartige Werte: [2 3 5 4 1]
- ***MaritalStatus*** 
<br>Datentyp: ***object*** 
<br>Bedeutung: Der Familienstand des Kunden
<br>Interpretation:
<br>einzigartige Werte: ['Single' 'Divorced' 'Married']
- ***NumberOfAddress*** 
<br>Datentyp: ***int64*** 
<br>Bedeutung: Die Anzahl der verschiedenen Lieferadressen eines Kunden
<br>Interpretation:
<br>einzigartige Werte: [ 9  7  6  8  3  2  4 10  1  5 19 21 11 20 22]
- ***Complain*** 
<br>Datentyp: ***int64*** 
<br>Bedeutung: Eine binäre Variable, die anzeigt, ob der Kunde in der Vergangenheit eine Beschwerde eingereicht hat.
<br>Interpretation: 1 = Ja ; 0 = Nein
<br>einzigartige Werte: [1 0]
- ***OrderAmountHikeFromlastYear*** 
<br>Datentyp: ***float64*** 
<br>Bedeutung: Die prozentuale Veränderung des Bestellbetrags im Vergleich zum Vorjahr.
<br>Interpretation:
<br>einzigartige Werte: [11. 15. 14. 23. 22. 16. 12. nan 13. 17. 18. 24. 19. 20. 21. 25. 26.]
- ***CouponUsed*** 
<br>Datentyp: ***float64*** 
<br>Bedeutung: Die Anzahl der Gutscheine oder Rabattcodes, die der Kunde verwendet hat.
<br>Interpretation:
<br>einzigartige Werte: [ 1.  0.  4.  2.  9.  6. 11. nan  7. 12. 10.  5.  3. 13. 15.  8. 14. 16.]
- ***OrderCount*** 
<br>Datentyp: ***float64*** 
<br>Bedeutung:  Die Gesamtanzahl der Bestellungen, die der Kunde aufgegeben hat.<br>Interpretation:
<br>einzigartige Werte: [ 1.  6.  2. 15.  4.  7.  3.  9. nan 11.  5. 12. 10.  8. 13. 14. 16.]
- ***DaySinceLastOrder*** 
<br>Datentyp: ***float64*** 
<br>Bedeutung: Die Anzahl der Tage seit der letzten Bestellung des Kunden.<br>Interpretation:
<br>einzigartige Werte: [ 5.  0.  3.  7.  2.  1.  8.  6.  4. 15.  9. 11. 10. nan 13. 12. 17. 16. 14. 30. 46. 18. 31.]
- ***CashbackAmount*** 
<br>Datentyp: ***float64*** 
<br>Bedeutung: Der Gesamtbetrag an Cashback, den der Kunde erhalten hat.<br>Interpretation:
<br>einzigartige Werte: [159.93 120.9  120.28 ... 173.77 287.91 173.78]
```python
# Variable und Datentyp usw. für jede Variable auszugeben
for column in df.columns:
    print(f"- ***{column}*** <br>Datentyp: ***{df[column].dtype}*** <br>Bedeutung: <br>Interpretation: <br>einzigartige Werte: {df[column].unique()}")
```

# Daten aufarbeiten
### Überflüssige Variablen
- Variable ***'CustomerID' Rausnehmen*** da dies eine uninteressante information für die Datenverarbeitung ist
```python
#Überflüssige Variablen entfernen

# axis=1 => axis ist ein Parameter in Pandas, der angibt,  entlang welcher Achse eine Operation in einem DataFrame oder einer Series durchgeführt werden soll. axis=0 bezieht sich auf die Zeilenachse, und axis=1 bezieht sich auf die Spaltenachse. 
df.drop('CustomerID', axis=1, inplace=True)
```
### Synonyme oder ähnliche Werte
- Variable ***'PreferredPaymentMode'*** Werte ***'Credit Card' und 'CC'*** sowie ***'Cash on Delivery' und 'COD' zusammenführen*** da die bezeichung Synonme sind und das selbe beschreiben
- Variable ***'PreferredOrderCat'*** Werte ***'Mobile' und 'Mobile Phone' Zusammenführen*** Zusammenführen da die bezeichnung Synonyme sind und das selbe beschreiben
```python
# Variable: 'PreferredOrderCat'
# Werte 'Mobile' und 'Mobile Phone' unter 'Mobile Device' Zusammenführen 
df['PreferedOrderCat'].replace(['Mobile', 'Mobile Phone'], 'Mobile Device', inplace=True)
```

```python
# Die Werte 'Mobile Phone' und 'Phone' der Variable 'PreferredLoginDevice' unter 'Mobile Device' zusammengeführt
df['PreferredLoginDevice'].replace(['Mobile Phone', 'Phone'], 'Mobile Device', inplace=True)
```

```python
# Die Werte 'Credit Card' und 'CC' der Variable 'PreferredPaymentMode' unter 'Credit Card' zusammengeführt
df['PreferredPaymentMode'].replace(['Credit Card', 'CC'], 'Credit Card', inplace=True)
```

```python
# Die Werte 'Cash on Delivery' und 'COD' der Variable 'PreferredPaymentMode' unter 'Cash on Delivery' zusammengeführt
df['PreferredPaymentMode'].replace(['Cash on Delivery', 'COD'], 'Cash on Delivery', inplace=True)
```
### Datentypen anpassen
- ***Datentyp bestehen lassen*** =>  Variablen ***'Tenure', 'WarehouseToHome', 'HourSpendOnApp', 'OrderAmountHikeFromLastYear'*** könnten in int64 umgewandelt werden. Zur weiteren berechnung wie bspw. den Durchschnitt wäre dies jedoch nicht sinnvoll da damit Information wegfallen würden.
### Umgang mit NaN-Werten
<details>
<summary>NaN Werte</summary>
CustomerID =                      0<br>
Churn =                           0<br>
Tenure =                        264<br>
PreferredLoginDevice =            0<br>
CityTier =                        0<br>
WarehouseToHome =               251<br>
PreferredPaymentMode =            0<br>
Gender =                          0<br>
HourSpendOnApp =                255<br>
NumberOfDeviceRegistered =        0<br>
PreferedOrderCat =                0<br>
SatisfactionScore =               0<br>
MaritalStatus =                   0<br>
NumberOfAddress =                 0<br>
Complain =                        0<br>
OrderAmountHikeFromlastYear =   265<br>
CouponUsed =                    256<br>
OrderCount =                    258<br>
</details>
<br>

- ***NaN Werte werden durch den Median der Jeweiligen Variable ersetzt*** Grund dafür ist das der Median resistenter gegen ausreißer ist (im gegensatz zum Durschnittswert). Das Entfernen von den zeilen mit den jeweiligen fehlenden Werten möchte vermieden werden da diese mehr als 5% des Datensatzes aus machen und dadurch Wichtige Informationen verloren gehen würden.
```Python
# NaN Werte ermitteln
df.isnull().sum()
```
```python
# NaN Werte ersetzen
for column in df:
    if df[column].dtype == object:
        continue
    # fillna() => umgang mit NaN werten
    # Inplace = True => gibt fest das dies über die Codezeile hinaus bestehen bleiben soll der Datensatz also fest verändert wird
    df[column].fillna(df[column].median(), inplace=True)
```
### Übertragen von Text in numerische Werte
- Variable: ***Gender, PreferredLoginDevice*** 
```python
# Die Variable Gender Nummerisch darstellen

df['Gender'].replace({'Male': 0, 'Female': 1}, inplace=True)
df['Gender'].unique()
```
```python
# Die Variable PreferredLoginDevice Nummerisch darstellen

df['PreferredLoginDevice'].replace({'Mobile Device': 0, 'Computer': 1}, inplace=True)
df['PreferredLoginDevice'].unique()
```
### Kategoriale Variablen in Dummy-Variablen („One hot encoding“) überführen
- Variablen: ***PreferredOrderCat, PreferredPaymentMode, MaritalStatus*** 
```python
# Erzeuge Dummy-Variablen für die Spalte 'PreferedOrderCat'
#
# prefix = Text der vor jedem Wert stehen wird
# pd.get_dummies => Automatsches Dummy erstellen durch panda
df_dummies = pd.get_dummies(df['PreferedOrderCat'], prefix='OrderCat')
# df_dummies erhält den Datentyp "bool" womit Machine Learning-Algorithmen jedoch auch rechenoperationen durchführen können sollten

# die Dummy-Variablen zum ursprünglichen DataFrame hinzufügen
# 
# pd.contact => die erstellten dummies zum df hinzufügen 
df_with_dummies = pd.concat([df, df_dummies], axis=1)
```
- Kategriale Variablen nach erzeugung der Dummy-Variablen entfernen

```pyhon
# Kategoriale Variablen die in Dummy-Variablen überfuhrt wurden Löschen

df_with_dummies.drop('PreferedOrderCat', axis=1, inplace=True)
df_with_dummies.drop('PreferredPaymentMode', axis=1, inplace=True)
df_with_dummies.drop('MaritalStatus', axis=1, inplace=True)
```

### Umgang mit Ausreißern
- *Ausreißer mittels IQR erkennen*

<details>
<summary>Ausreißer:</summary>
Variable: Tenure
<br>Durschnitt: 10.134103019538188
<br>Median: 8.357951166584485
<br>Minimum: 0
<br>Maximum: 61
<br>Q1(0,25): 3.0
<br>Q3(0,75): 15.0
<br>IQR: 12.0
<br>Anzahl an Ausreißern: 4
<br>Ausreißer:
50<br>
60<br>
51<br>
61<br>


Variable: CityTier
<br>Durschnitt: 1.6547069271758437
<br>Median: 0.9153892691210666
<br>Minimum: 1
<br>Maximum: 3
<br>Q1(0,25): 1.0
<br>Q3(0,75): 3.0
<br>IQR: 2.0
<br>Anzahl an Ausreißern: 0
<br>Ausreißer:


Variable: WarehouseToHome
<br>Durschnitt: 15.566785079928952
<br>Median: 8.345961296394036
<br>Minimum: 5.0
<br>Maximum: 127.0
<br>Q1(0,25): 9.0
<br>Q3(0,75): 20.0
<br>IQR: 11.0
<br>Anzahl an Ausreißern: 2
<br>Ausreißer:
126.0<br>
127.0<br>


Variable: HourSpendOnApp
<br>Durschnitt: 2.9346358792184724
<br>Median: 0.7055280039478681
<br>Minimum: 0.0
<br>Maximum: 5.0
<br>Q1(0,25): 2.0
<br>Q3(0,75): 3.0
<br>IQR: 1.0
<br>Anzahl an Ausreißern: 6
<br>Ausreißer:
0.0<br>
0.0<br>
0.0<br>
5.0<br>
5.0<br>
5.0<br>


Variable: NumberOfDeviceRegistered
<br>Durschnitt: 3.68898756660746
<br>Median: 1.0239985188585785
<br>Minimum: 1
<br>Maximum: 6
<br>Q1(0,25): 3.0
<br>Q3(0,75): 4.0
<br>IQR: 1.0
<br>Anzahl an Ausreißern: 397
<br>Ausreißer:
Die ausreißer stellen mehr als 5% der Werte der Variable da<br>

Variable: NumberOfAddress
<br>Durschnitt: 4.214031971580817
<br>Median: 2.5835855126063794
<br>Minimum: 1
<br>Maximum: 22
<br>Q1(0,25): 2.0
<br>Q3(0,75): 6.0
<br>IQR: 4.0
<br>Anzahl an Ausreißern: 4
<br>Ausreißer:
19<br>
21<br>
20<br>
22<br>


Variable: OrderAmountHikeFromlastYear
<br>Durschnitt: 15.674600355239788
<br>Median: 3.5910576608583926
<br>Minimum: 11.0
<br>Maximum: 26.0
<br>Q1(0,25): 13.0
<br>Q3(0,75): 18.0
<br>IQR: 5.0
<br>Anzahl an Ausreißern: 33
<br>Ausreißer:
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>
26.0<br>


Variable: CouponUsed
<br>Durschnitt: 1.7168738898756661
<br>Median: 1.857639777461501
<br>Minimum: 0.0
<br>Maximum: 16.0
<br>Q1(0,25): 1.0
<br>Q3(0,75): 2.0
<br>IQR: 1.0
<br>Anzahl an Ausreißern: 629
<br>Ausreißer:
Die ausreißer stellen mehr als 5% der Werte der Variable da<br>

Variable: OrderCount
<br>Durschnitt: 2.9618117229129663
<br>Median: 2.8792477181293767
<br>Minimum: 1.0
<br>Maximum: 16.0
<br>Q1(0,25): 1.0
<br>Q3(0,75): 3.0
<br>IQR: 2.0
<br>Anzahl an Ausreißern: 703
<br>Ausreißer:
Die ausreißer stellen mehr als 5% der Werte der Variable da<br>

Variable: DaySinceLastOrder
<br>Durschnitt: 4.459325044404974
<br>Median: 3.570625540419597
<br>Minimum: 0.0
<br>Maximum: 46.0
<br>Q1(0,25): 2.0
<br>Q3(0,75): 7.0
<br>IQR: 5.0
<br>Anzahl an Ausreißern: 62
<br>Ausreißer:
15.0<br>
15.0<br>
15.0<br>
17.0<br>
16.0<br>
17.0<br>
15.0<br>
17.0<br>
17.0<br>
17.0<br>
17.0<br>
16.0<br>
17.0<br>
15.0<br>
30.0<br>
15.0<br>
15.0<br>
15.0<br>
17.0<br>
16.0<br>
17.0<br>
15.0<br>
17.0<br>
46.0<br>
17.0<br>
17.0<br>
17.0<br>
16.0<br>
16.0<br>
16.0<br>
16.0<br>
18.0<br>
17.0<br>
18.0<br>
16.0<br>
18.0<br>
15.0<br>
15.0<br>
18.0<br>
18.0<br>
15.0<br>
15.0<br>
17.0<br>
15.0<br>
16.0<br>
31.0<br>
16.0<br>
16.0<br>
16.0<br>
18.0<br>
17.0<br>
18.0<br>
16.0<br>
18.0<br>
15.0<br>
15.0<br>
18.0<br>
18.0<br>
15.0<br>
15.0<br>
17.0<br>
15.0<br>


Variable: CashbackAmount
<br>Durschnitt: 177.22303019538188
<br>Median: 49.20703617486409
<br>Minimum: 0.0
<br>Maximum: 324.99
<br>Q1(0,25): 145.77
<br>Q3(0,75): 196.3925
<br>IQR: 50.6225
<br>Anzahl an Ausreißern: 438
<br>Ausreißer:
Die ausreißer stellen mehr als 5% der Werte der Variable da<br>
</details>

```python
# Ausreißer ausgeben 
for column in df:
    if df[column].dtype == 'object' or column == 'Churn' or column == 'PreferredLoginDevice' or column == 'City Tier' or column == 'SatisfactionScore' or column == 'Gender' or column == 'Complain':
        continue
    Q1 = df[column].quantile(0.25)
    Q3 = df[column].quantile(0.75)
    IQR = Q3 - Q1
    outliers = df[(df[column] < Q1 - 1.5 * IQR) | (df[column] > Q3 + 1.5 * IQR)]
    print(f"Variable: {column}")
    print(f"<br>Durschnitt: {df[column].mean()}")
    print(f"<br>Median: {df[column].std()}")
    print(f"<br>Minimum: {df[column].min()}")
    print(f"<br>Maximum: {df[column].max()}")
    print(f"<br>Q1(0,25): {Q1}")
    print(f"<br>Q3(0,75): {Q3}")
    print(f"<br>IQR: {IQR}")
    print(f"<br>Anzahl an Ausreißern: {outliers[column].size}")
    print("<br>Ausreißer:")
    if outliers[column].size >= 280:
            print("Die ausreißer stellen mehr als 5% der Werte der Variable da<br>\n")
            continue
    for outlier in outliers[column]:
         print(f"{outlier}<br>")
    print("\n")
```

- ***Ausreißer kappen*** Werte, die einen bestimmten Schwellenwert (Q1 - 1.5 * IQR bzw. Q3 + 1.5 * IQR) überschreiten, werden auf diesen Schwellenwert reduziert.<br> Grund: wir wollen wissen was in einem "Typischen Fall" dazu führt das jemand von dem Unternehmen abwandert und suchen nicht nach Anomalyen
<br>***Ausreißer > 5% des Datensatzes nicht kappen*** 
<br>Grund: Ein zu großer Informationsverlust ergibt sich und für diese Variablen werden die "Ausreißer" nicht als echte Ausreißer angesehen
```python
for column in df:
    if df[column].dtype == 'object' or column in ['Churn', 'PreferredLoginDevice', 'CityTier', 'SatisfactionScore', 'Gender', 'Complain', 'NumberOfDeviceRegistered', 'CouponUsed', 'OrderCount', 'CashbackAmount']:
        continue
    Q1 = df[column].quantile(0.25)
    Q3 = df[column].quantile(0.75)
    IQR = Q3 - Q1
    
    lower_bound = Q1 - 1.5 * IQR
    upper_bound = Q3 + 1.5 * IQR
    #Die Methode clip begrenzt die Werte einer Serie auf ein gegebenes Intervall, das durch die Argumente lower und upper festgelegt wird. In diesem Fall setzen wir die Werte unter Q1 - 1.5 * IQR auf Q1 - 1.5 * IQR und die Werte über Q3 + 1.5 * IQR auf Q3 + 1.5 * IQR, wodurch die Ausreißer effektiv gekappt werden.
    df[column] = df[column].clip(lower=lower_bound, upper=upper_bound)
```

### Werte der Variablen auf ein Skalenniveau bringen (Normalisieren)
- Verwendung der ***Min-Max-Normalisierung*** auf die kontinuierlichen Merkmale `Tenure`, `WarehouseToHome`, `HourSpendOnApp`, `NumberOfDeviceRegistered`, `OrderAmountHikeFromlastYear`, `CouponUsed`, `OrderCount`, `DaySinceLastOrder`, und `CashbackAmount` angewandt, um sicherzustellen, dass jedes Merkmal gleich gewichtet wird. Dies wurde durchgeführt, um den Einfluss unterschiedlicher Wertebereiche auf das Vorhersagemodell zu minimieren.

<details>
<summary>min, max werte der Ausprägungen</summary>

<br>- ***Tenure*** <br>***Min:*** 0.0 <br>***Max:*** 61.0<br>
<br>- ***WarehouseToHome*** <br>***Min:*** 5.0 <br>***Max:*** 127.0<br>
<br>- ***HourSpendOnApp*** <br>***Min:*** 0.0 <br>***Max:*** 5.0<br>
<br>- ***NumberOfDeviceRegistered*** <br>***Min:*** 1.0 <br>***Max:*** 6.0<br>
<br>- ***NumberOfAddress*** <br>***Min:*** 1.0 <br>***Max:*** 22.0<br>
<br>- ***OrderAmountHikeFromlastYear*** <br>***Min:*** 11.0 <br>***Max:*** 26.0<br>
<br>- ***CouponUsed*** <br>***Min:*** 0.0 <br>***Max:*** 16.0<br>
<br>- ***OrderCount*** <br>***Min:*** 1.0 <br>***Max:*** 16.0<br>
<br>- ***DaySinceLastOrder*** <br>***Min:*** 0.0 <br>***Max:*** 46.0<br>
<br>- ***CashbackAmount*** <br>***Min:*** 0.0 <br>***Max:*** 324.99<br>
</details>

```python
# Normalisieren mittels Min-Max-Normalisierung
from sklearn.preprocessing import MinMaxScaler

features_to_normalize = [
    'Tenure',
    'WarehouseToHome',
    'HourSpendOnApp',
    'NumberOfDeviceRegistered',
    'NumberOfAddress',
    'OrderAmountHikeFromlastYear',
    'CouponUsed',
    'OrderCount',
    'DaySinceLastOrder',
    'CashbackAmount'
]


# MinMaxScaler initialisieren
scaler = MinMaxScaler()

scaler.fit(df_with_dummies[features_to_normalize])

# Features im scaler 
print(scaler.feature_names_in_)

# Feature Ausprägungen ausgeben
i = 0
for column in features_to_normalize:
     print(f"<br>- ***{column}*** <br>***Min:*** {scaler.data_min_[i]} <br>***Max:*** {scaler.data_max_[i]}<br>")
     i += 1


#-------------------------------------------------------------------------------#

# Feature Normalisieren
# Die transform-Methode des MinMaxScaler gibt ein Numpy-Array zurück
features_normalized_NumpArray = scaler.transform(df_with_dummies[features_to_normalize])


# Konvertieren des Numpy-Arrays zurück in einen DataFrame
df_normalized = pd.DataFrame(features_normalized_NumpArray, columns=features_to_normalize)

# Sicherstellen das der Index (Die zeilen beider Dataframes) gleich sind
df_normalized.index = df_with_dummies.index

# neues df erstellen 
df_with_dummies_and_normalized = df_with_dummies

# das Dataframe mit den Spalten aus den normalisierten Spalten ersetzten
for column in features_to_normalize:
    df_with_dummies_and_normalized[column] = df_normalized[column]
```
### Bool werte nummerisch dargestellt 

```python
# boolische werte in nummerische umwandeln 
df_with_dummies_and_normalized_and_nummeric = df_with_dummies_and_normalized

for column in df_with_dummies_and_normalized_and_nummeric.columns:
    if df_with_dummies_and_normalized_and_nummeric[column].dtype == 'bool':
        print(column)
        df_with_dummies_and_normalized_and_nummeric[column] = df_with_dummies_and_normalized_and_nummeric[column].astype(int)

df_with_dummies_and_normalized_and_nummeric.head()
```



# Aufgearbeiteter Datensatz

<details>
<summary>Vor der Normalisierung</summary>

- ***Churn*** 
<br>Datentyp: ***int64*** 
<br>Interpretation: 1 = ja ; 0 = nein
<br>einzigartige Werte: [1 0]
- ***Tenure*** 
<br>Datentyp: ***int32*** 
<br>Interpretation: Dauer in Monaten
<br>einzigartige Werte: [ 4  9  0 13 11 19 20 14  8 18  5  2 30  1 23  3 29  6 26 28  7 24 25 10
 15 22 27 16 12 21 17 50 60 31 51 61]
- ***PreferredLoginDevice*** 
<br>Datentyp: ***int64*** 
<br>Interpretation: 
<br>einzigartige Werte: [0 1]
- ***CityTier*** 
<br>Datentyp: ***int64*** 
<br>Interpretation: Es könnte 1 für Großstädte, 2 für mittelgroße Städte und 3 für kleine Städte stehen.
<br>einzigartige Werte: [3 1 2]
- ***WarehouseToHome*** 
<br>Datentyp: ***float64*** 
<br>Interpretation: Entfernung In Kilometern
<br>einzigartige Werte: [  6.   8.  30.  15.  12.  22.  11.   9.  31.  18.  13.  20.  29.  28.
  26.  14.  10.  27.  17.  23.  33.  19.  35.  24.  16.  25.  32.  34.
   5.  21. 126.   7.  36. 127.]
- ***PreferredPaymentMode*** 
<br>Datentyp: ***object*** 
<br>Interpretation: 
<br>einzigartige Werte: ['Debit Card' 'UPI' 'Credit Card' 'Cash on Delivery' 'E wallet']
- ***Gender*** 
<br>Datentyp: ***int64*** 
<br>Interpretation: 
<br>einzigartige Werte: [1 0]
- ***HourSpendOnApp*** 
<br>Datentyp: ***float64*** 
<br>Interpretation: 
<br>einzigartige Werte: [3. 2. 1. 0. 4. 5.]
- ***NumberOfDeviceRegistered*** 
<br>Datentyp: ***int64*** 
<br>Interpretation: 
<br>einzigartige Werte: [3 4 5 2 1 6]
- ***PreferedOrderCat*** 
<br>Datentyp: ***object*** 
<br>Interpretation: 
<br>einzigartige Werte: ['Laptop & Accessory' 'Mobile Device' 'Others' 'Fashion' 'Grocery']
- ***SatisfactionScore*** 
<br>Datentyp: ***int64*** 
<br>Interpretation: 
<br>einzigartige Werte: [2 3 5 4 1]
- ***MaritalStatus*** 
<br>Datentyp: ***object*** 
<br>Interpretation: 
<br>einzigartige Werte: ['Single' 'Divorced' 'Married']
- ***NumberOfAddress*** 
<br>Datentyp: ***int64*** 
<br>Interpretation: 
<br>einzigartige Werte: [ 9  7  6  8  3  2  4 10  1  5 19 21 11 20 22]
- ***Complain*** 
<br>Datentyp: ***int64*** 
<br>Interpretation: 0 = Keine Beschwerde eingereicht; 1 = Eine Beschwerde Eingereicht
<br>einzigartige Werte: [1 0]
- ***OrderAmountHikeFromlastYear*** 
<br>Datentyp: ***float64*** 
<br>Interpretation: 
<br>einzigartige Werte: [11. 15. 14. 23. 22. 16. 12. 13. 17. 18. 24. 19. 20. 21. 25. 26.]
- ***CouponUsed*** 
<br>Datentyp: ***float64*** 
<br>Interpretation: 
<br>einzigartige Werte: [ 1.  0.  4.  2.  9.  6. 11.  7. 12. 10.  5.  3. 13. 15.  8. 14. 16.]
- ***OrderCount*** 
<br>Datentyp: ***float64*** 
<br>Interpretation: 
<br>einzigartige Werte: [ 1.  6.  2. 15.  4.  7.  3.  9. 11.  5. 12. 10.  8. 13. 14. 16.]
- ***DaySinceLastOrder*** 
<br>Datentyp: ***float64*** 
<br>Interpretation: 
<br>einzigartige Werte: [ 5.  0.  3.  7.  2.  1.  8.  6.  4. 15.  9. 11. 10. 13. 12. 17. 16. 14. 30. 46. 18. 31.]
- ***CashbackAmount*** 
<br>Datentyp: ***float64*** 
<br>Interpretation: 
<br>einzigartige Werte: [159.93 120.9  120.28 ... 173.77 287.91 173.78]
- ***OrderCat_Fashion*** 
<br>Datentyp: ***bool*** 
<br>Interpretation: 
<br>einzigartige Werte: [False  True]
- ***OrderCat_Grocery*** 
<br>Datentyp: ***bool*** 
<br>Interpretation: 
<br>einzigartige Werte: [False  True]
- ***OrderCat_Laptop & Accessory*** 
<br>Datentyp: ***bool*** 
<br>Interpretation: 
<br>einzigartige Werte: [ True False]
- ***OrderCat_Mobile Device*** 
<br>Datentyp: ***bool*** 
<br>Interpretation: 
<br>einzigartige Werte: [False  True]
- ***OrderCat_Others*** 
<br>Datentyp: ***bool*** 
<br>Interpretation: 
<br>einzigartige Werte: [False  True]
- ***PaymentMode_Cash on Delivery*** 
<br>Datentyp: ***bool*** 
<br>Interpretation: 
<br>einzigartige Werte: [False  True]
- ***PaymentMode_Credit Card*** 
<br>Datentyp: ***bool*** 
<br>Interpretation: 
<br>einzigartige Werte: [False  True]
- ***PaymentMode_Debit Card*** 
<br>Datentyp: ***bool*** 
<br>Interpretation: 
<br>einzigartige Werte: [ True False]
- ***PaymentMode_E wallet*** 
<br>Datentyp: ***bool*** 
<br>Interpretation: 
<br>einzigartige Werte: [False  True]
- ***PaymentMode_UPI*** 
<br>Datentyp: ***bool*** 
<br>Interpretation: 
<br>einzigartige Werte: [False  True]
- ***MartialStatus_Divorced*** 
<br>Datentyp: ***bool*** 
<br>Interpretation: 
<br>einzigartige Werte: [False  True]
- ***MartialStatus_Married*** 
<br>Datentyp: ***bool*** 
<br>Interpretation: 
<br>einzigartige Werte: [False  True]
- ***MartialStatus_Single*** 
<br>Datentyp: ***bool*** 
<br>Interpretation: 
<br>einzigartige Werte: [ True False]

</details>

<details>
<summary>Nach der Normalisierung</summary>

- 0 für `False`, 1 für `True`

- ***Churn*** 
<br>Datentyp: ***int64*** 
<br>Interpretation: 
<br>einzigartige Werte: [1 0]
- ***Tenure*** 
<br>Datentyp: ***float64*** 
<br>Interpretation: 
<br>einzigartige Werte: [0.12121212 0.27272727 0.         0.39393939 0.33333333 0.57575758
 0.60606061 0.42424242 0.24242424 0.54545455 0.15151515 0.06060606
 0.90909091 0.03030303 0.6969697  0.09090909 0.87878788 0.18181818
 0.78787879 0.84848485 0.21212121 0.72727273 0.75757576 0.3030303
 0.45454545 0.66666667 0.81818182 0.48484848 0.36363636 0.63636364
 0.51515152 1.         0.93939394]
- ***PreferredLoginDevice*** 
<br>Datentyp: ***int64*** 
<br>Interpretation: 
<br>einzigartige Werte: [0 1]
- ***CityTier*** 
<br>Datentyp: ***int64*** 
<br>Interpretation: 
<br>einzigartige Werte: [3 1 2]
- ***WarehouseToHome*** 
<br>Datentyp: ***float64*** 
<br>Interpretation: 
<br>einzigartige Werte: [0.03174603 0.0952381  0.79365079 0.31746032 0.22222222 0.53968254
 0.19047619 0.12698413 0.82539683 0.41269841 0.25396825 0.47619048
 0.76190476 0.73015873 0.66666667 0.28571429 0.15873016 0.6984127
 0.38095238 0.57142857 0.88888889 0.44444444 0.95238095 0.6031746
 0.34920635 0.63492063 0.85714286 0.92063492 0.         0.50793651 1.   0.06349206 0.98412698]
- ***Gender*** 
<br>Datentyp: ***int64*** 
<br>Interpretation: 
<br>einzigartige Werte: [1 0]
- ***HourSpendOnApp*** 
<br>Datentyp: ***float64*** 
<br>Interpretation: 
<br>einzigartige Werte: [0.625 0.375 0.125 0.    0.875 1.   ]
- ***NumberOfDeviceRegistered*** 
<br>Datentyp: ***float64*** 
<br>Interpretation: 
<br>einzigartige Werte: [0.4 0.6 0.8 0.2 0.  1. ]
- ***SatisfactionScore*** 
<br>Datentyp: ***int64*** 
<br>Interpretation: 
<br>einzigartige Werte: [2 3 5 4 1]
- ***NumberOfAddress*** 
<br>Datentyp: ***float64*** 
<br>Interpretation: 
<br>einzigartige Werte: [0.72727273 0.54545455 0.45454545 0.63636364 0.18181818 0.09090909
 0.27272727 0.81818182 0.         0.36363636 1.         0.90909091]
- ***Complain*** 
<br>Datentyp: ***int64*** 
<br>Interpretation: 
<br>einzigartige Werte: [1 0]
- ***OrderAmountHikeFromlastYear*** 
<br>Datentyp: ***float64*** 
<br>Interpretation: 
<br>einzigartige Werte: [0.         0.27586207 0.20689655 0.82758621 0.75862069 0.34482759
 0.06896552 0.13793103 0.4137931  0.48275862 0.89655172 0.55172414
 0.62068966 0.68965517 0.96551724 1.        ]
- ***CouponUsed*** 
<br>Datentyp: ***float64*** 
<br>Interpretation: 
<br>einzigartige Werte: [0.0625 0.     0.25   0.125  0.5625 0.375  0.6875 0.4375 0.75   0.625
 0.3125 0.1875 0.8125 0.9375 0.5    0.875  1.    ]
- ***OrderCount*** 
<br>Datentyp: ***float64*** 
<br>Interpretation: 
<br>einzigartige Werte: [0.         0.33333333 0.06666667 0.93333333 0.2        0.4
 0.13333333 0.53333333 0.66666667 0.26666667 0.73333333 0.6
 0.46666667 0.8        0.86666667 1.        ]
- ***DaySinceLastOrder*** 
<br>Datentyp: ***float64*** 
<br>Interpretation: 
<br>einzigartige Werte: [0.34482759 0.         0.20689655 0.48275862 0.13793103 0.06896552
 0.55172414 0.4137931  0.27586207 1.         0.62068966 0.75862069
 0.68965517 0.89655172 0.82758621 0.96551724]
- ***CashbackAmount*** 
<br>Datentyp: ***float64*** 
<br>Interpretation: 
<br>einzigartige Werte: [0.49210745 0.37201145 0.3701037  ... 0.53469338 0.88590418 0.53472415]
- ***OrderCat_Fashion*** 
<br>Datentyp: ***int32*** 
<br>Interpretation: 
<br>einzigartige Werte: [0 1]
- ***OrderCat_Grocery*** 
<br>Datentyp: ***int32*** 
<br>Interpretation: 
<br>einzigartige Werte: [0 1]
- ***OrderCat_Laptop & Accessory*** 
<br>Datentyp: ***int32*** 
<br>Interpretation: 
<br>einzigartige Werte: [1 0]
- ***OrderCat_Mobile Device*** 
<br>Datentyp: ***int32*** 
<br>Interpretation: 
<br>einzigartige Werte: [0 1]
- ***OrderCat_Others*** 
<br>Datentyp: ***int32*** 
<br>Interpretation: 
<br>einzigartige Werte: [0 1]
- ***PaymentMode_Cash on Delivery*** 
<br>Datentyp: ***int32*** 
<br>Interpretation: 
<br>einzigartige Werte: [0 1]
- ***PaymentMode_Credit Card*** 
<br>Datentyp: ***int32*** 
<br>Interpretation: 
<br>einzigartige Werte: [0 1]
- ***PaymentMode_Debit Card*** 
<br>Datentyp: ***int32*** 
<br>Interpretation: 
<br>einzigartige Werte: [1 0]
- ***PaymentMode_E wallet*** 
<br>Datentyp: ***int32*** 
<br>Interpretation: 
<br>einzigartige Werte: [0 1]
- ***PaymentMode_UPI*** 
<br>Datentyp: ***int32*** 
<br>Interpretation: 
<br>einzigartige Werte: [0 1]
- ***MartialStatus_Divorced*** 
<br>Datentyp: ***int32*** 
<br>Interpretation: 
<br>einzigartige Werte: [0 1]
- ***MartialStatus_Married*** 
<br>Datentyp: ***int32*** 
<br>Interpretation: 
<br>einzigartige Werte: [0 1]
- ***MartialStatus_Single*** 
<br>Datentyp: ***int32*** 
<br>Interpretation: 
<br>einzigartige Werte: [1 0]
</details>


```python
# Erneutes ausgeben der Variablen und dessen werte für den Überarbeiteten Datensatz vor der Normalisierung: 

for column in df_with_dummies.columns:
    print(f"- ***{column}*** \n<br>Datentyp: ***{df_with_dummies[column].dtype}*** \n<br>Interpretation: \n<br>einzigartige Werte: {df_with_dummies[column].unique()}")
```


```python
# Erneutes ausgeben der Variablen und dessen werte für den Überarbeiteten Datensatz nach der Normalisierung: 

for column in df_with_dummies.columns:
    print(f"- ***{column}*** \n<br>Datentyp: ***{df_with_dummies[column].dtype}*** \n<br>Interpretation: \n<br>einzigartige Werte: {df_with_dummies[column].unique()}")
```