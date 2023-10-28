# Deskriptive und Explorative beschreibung "Ecommerce Customer Churn"


### [Über Den Datensatz](#der-datensatz)

# Der Datensatz

### Datenquelle
https://www.kaggle.com/datasets/ankitverma2010/ecommerce-customer-churn-analysis-and-prediction


## Column header description and interpretation:
- ***CustomerID*** <br>Datentyp: ***int64*** <br>Bedeutung: Dies ist eine eindeutige Kennung oder Identifikationsnummer für jeden Kunden.  <br>Interpretation:
- ***Churn*** <br>Datentyp: ***int64*** <br>Bedeutung: Dies ist eine binäre Variable, die angibt, ob ein Kunde abgewandert ist oder nicht. <br>Interpretation:
- ***Tenure*** <br>Datentyp: ***float64*** <br>Bedeutung: Dies ist die Dauer oder Zeitspanne, die ein Kunde bereits Kunde ist  <br>Interpretation:
- ***PreferredLoginDevice*** <br>Datentyp: ***object*** <br>Bedeutung: Dies gibt an, welches Gerät der Kunde bevorzugt, um sich bei seinem Konto anzumelden<br>Interpretation:
- ***CityTier*** <br>Datentyp: ***int64*** <br>Bedeutung: Dies ist eine Kategorisierung der Stadt, in der der Kunde lebt <br>Interpretation:
- ***WarehouseToHome*** <br>Datentyp: ***float64*** <br>Bedeutung: Die durchschnittliche Entfernung zum Wohnort des Kunden<br>Interpretation:
- ***PreferredPaymentMode*** <br>Datentyp: ***object*** <br>Bedeutung: Dies gibt die bevorzugte Zahlungsmethode des Kunden an<br>Interpretation:
- ***Gender*** <br>Datentyp: ***object*** <br>Bedeutung: Das Geschlecht des Kunden<br>Interpretation:
- ***HourSpendOnApp*** <br>Datentyp: ***float64*** <br>Bedeutung: Die durchschnittliche Zeit, die der Kunde täglich auf der Unternehmens-App verbringt<br>Interpretation:
- ***NumberOfDeviceRegistered*** <br>Datentyp: ***int64*** <br>Bedeutung:  Die Anzahl der Geräte, die der Kunde bei dem Unternehmen registriert hat.<br>Interpretation:
- ***PreferedOrderCat*** <br>Datentyp: ***object*** <br>Bedeutung: Die bevorzugte Kategorie von Produkten oder Dienstleistungen, die der Kunde bestellt<br>Interpretation:
- ***SatisfactionScore*** <br>Datentyp: ***int64*** <br>Bedeutung: Dies ist eine Bewertung die die Zufriedenheit des Kunden wiederspiegelt<br>Interpretation:
- ***MaritalStatus*** <br>Datentyp: ***object*** <br>Bedeutung: Der Familienstand des Kunden<br>Interpretation:
- ***NumberOfAddress*** <br>Datentyp: ***int64*** <br>Bedeutung: Die Anzahl der verschiedenen Lieferadressen<br>Interpretation:
- ***Complain*** <br>Datentyp: ***int64*** <br>Bedeutung: Eine binäre Variable, die anzeigt, ob der Kunde in der Vergangenheit eine Beschwerde eingereicht hat.<br>Interpretation:
- ***OrderAmountHikeFromlastYear*** <br>Datentyp: ***float64*** <br>Bedeutung: Die prozentuale Veränderung des Bestellbetrags im Vergleich zum Vorjahr.<br>Interpretation:
- ***CouponUsed*** <br>Datentyp: ***float64*** <br>Bedeutung: Die Anzahl der Gutscheine oder Rabattcodes, die der Kunde verwendet hat.<br>Interpretation:
- ***OrderCount*** <br>Datentyp: ***float64*** <br>Bedeutung:  Die Gesamtanzahl der Bestellungen, die der Kunde aufgegeben hat.<br>Interpretation:
- ***DaySinceLastOrder*** <br>Datentyp: ***float64*** <br>Bedeutung: Die Anzahl der Tage seit der letzten Bestellung des Kunden.<br>Interpretation:
- ***CashbackAmount*** <br>Datentyp: ***float64*** <br>Bedeutung: Der Gesamtbetrag an Cashback, den der Kunde erhalten hat.<br>Interpretation:
## Daten Filtern
- 'CustomerID' Rausnehmen da dies eine uninteressante information für die Datenverarbeitung ist
- 