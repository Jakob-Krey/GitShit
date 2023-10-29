# Deskriptive und Explorative beschreibung "Ecommerce Customer Churn"


### [Über Den Datensatz](#der-datensatz)

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

## Verwendeter Code

<details open>

```
# Variable und Datentyp ausgeben
for column in df.columns:
    print(f"- ***{column}*** <br>Datentyp: ***{df[column].dtype}*** <br>Bedeutung: <br>Interpretation:")
```

```
# Jeden einzigartigen Wert einer Variablen ausgeben
for column_header in df.columns:
    print(f"{column_header}  <br>einzigartige Werte: {df[column_header].unique()}")
```
</details>

## Daten bereinigen
### Überflüssige Varialen 
- Variable ***'CustomerID' Rausnehmen*** da dies eine uninteressante information für die Datenverarbeitung ist
### Synonyme oder ähnliche Werte
- Variable ***'PreferredPaymentMode'*** Werte ***'Credit Card' und 'CC'*** sowie ***'Cash on Delivery' und 'COD' zusammenführen*** da die bezeichung Synonme sind und das selbe beschreiben
- Variable ***'PreferredOrderCat'*** Werte ***'Mobile' und 'Mobile Phone' Zusammenführen*** Zusammenführen da die bezeichnung Synonyme sind und das selbe beschreiben
### Datentypen anpassen
- Variablen ***'Tenure', 'WarehouseToHome', 'HourSpendOnApp', 'OrderAmountHikeFromLastYear'*** könnten in int64 umgewandelt werden. Zur weiteren berechnung wie bspw. den Durchschnitt wäre dies jedoch nicht sinnvoll da damit Information wegfallen würden daher => ***Datentyp bestehn lassen***
### Umgang mit NaN-Werten

```
# Jeden einzigartigen Wert einer Variablen ausgeben
for column_header in df.columns:
    print(f"{column_header}  <br>einzigartige Werte: {df[column_header].unique()}")
```
  