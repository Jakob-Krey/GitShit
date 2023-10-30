# Deskriptive und Explorative beschreibung "Ecommerce Customer Churn"


### [Über Den Datensatz](#der-datensatz)
### [Aufarbeiteung des Datensatzes](#daten-bereinigen)
### [Der Aufgearbeitete Datensatz](#aufgearbeiteter-datensatz)

# Der Datensatz

### Datenquelle
https://www.kaggle.com/datasets/ankitverma2010/ecommerce-customer-churn-analysis-and-prediction


## Column header description and interpretation:
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

# Aufgearbeiteter Datensatz
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

```python
# Erneutes ausgeben der Variablen und dessen werte fr den Überarbeiteten Datensatz: 

for column in df_with_dummies.columns:
    print(f"- ***{column}*** \n<br>Datentyp: ***{df_with_dummies[column].dtype}*** \n<br>Interpretation: \n<br>einzigartige Werte: {df_with_dummies[column].unique()}")
```