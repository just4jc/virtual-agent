---

copyright:
  years: 2015, 2017
lastupdated: "2017-09-27"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}
{:pre: .pre}
{:codeblock: .codeblock}
{:screen: .screen}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:swift: .ph data-hd-programlang='swift'}

# Absichtsnamen (Retail Banking)
{: #intent_codenames_banking}
{: #top}

[![Zurück](images/back-arrow.png)](intent_codenames.html)

In der folgenden Tabelle werden die Absichtsnamen der einzelnen unterstützten Funktionen aufgelistet. Wenn Sie für eine Funktion Ihren eigenen {{site.data.keyword.conversationshort}}-Servicedialog bereitstellen möchten, muss Ihnen der entsprechende Absichtsname bekannt sein, damit Sie diesen im Dialog angeben können. Sie können den Namen hier suchen.
{: shortdesc}

| Zentrale Funktionen             | Funktion zugeordneter Absichtsname                     |
|---------------------------------|--------------------------------------------------------|
| Abfrage des Kontostands | #Billing-Balance_Inquiry |
| Abrechnung allgemein | #Billing-Misc |
| Adresse aktualisieren`*` | #Account_Management-Update_Change_Address |
| Aktivität anzeigen | #Checking_Savings_Accounts-View_Activity |
| Aktualisierung der Zahlungsart | #Payment-Method_Of_Payment_Update |
| Akzeptierte Zahlungsarten | #Payment-Method_Of_Payment_Inquiry |
| Allgemeine Informationen | #Information-Misc |
| Anfordern der Vereinbarung über die Kartenmitgliedschaft | #Credit_Card_Account_Services-Request_Card_Member_Agreement |
| Anfrage der Rechnungsanschrift | #Account_Management-Billing_Address_Inquiry |
| Ausgabenschwellenwert | #Alerts-Account_Alerts_Spending_Threshold |
| Ausstehende Gebühren anzeigen | #Credit_Card_Account_Services-View_Pending_Charges |
| Bankdaten | #Payment-Bank_Information |
| Bankleitzahl anzeigen | #Checking_Savings_Accounts-View_Routing_Number |
| Banküberweisungen | #Checking_Savings_Accounts-Wire_Funds |
| Beendung | #Help-Ending |
| Begrüßung | #Help-Greetings |
| Benachrichtigung über Geschäftsreisen`*` | #Alerts-Account_Alerts_Travel |
| Berechtigte Benutzer | #Account_Management-Authorized_User |
| Bürotermin vereinbaren | #Information-Make_Store_Appointment |
| Bürotermin verschieben | #Information-Change_Store_Appointment |
| Dienstleistungen einer Filiale | #Information-Store_Services |
| Direktüberweisungen einrichten | #Checking_Savings_Accounts-Set_Up_Direct_Deposit |
| E-Mail aktualisieren`*` | #Account_Management-Email_Change |
| Eine Zahlung tätigen`*` | #Payment-Make_A_Payment |
| Erhöhung des Kreditrahmens anfordern | #Credit_Card_Account_Services-Request_Increase_In_Credit_Line |
| Erstattung | #Payment-Refund_Payment |
| Fehlende oder falsche Zahlungen | #Payment-Missing_Misapplied_Payment |
| Gebuchte Zahlungen | #Alerts-Account_Alerts_Payment_Posted |
| Gebührenanfrage | #Credit_Card_Account_Services-Fee_Inquiry |
| Geldüberweisung | #Checking_Savings_Accounts-Transfer_Money |
| Hilfe | #Help-Help |
| Karte aktivieren`*` | #Credit_Card_Account_Services-Activate_A_Card |
| Karte ersetzen`*` | #Credit_Card_Account_Services-Replace_A_Card |
| Keines der Obigen | #Off_Topic-None_of_the_Above |
| Kontakt | #Information-Contact_Us |
| Konto eröffnen | #Account_Management-Open_Account |
| Konto löschen | #Account_Management-Close_Cancel_Account |
| Kontoberechtigungen | #Account_Management-Privileges |
| Kontonamensänderung | #Account_Management-Name_Change |
| Kontoverwaltung allgemein | #Account_Management-Misc |
| Kreditkarte kündigen | #Credit_Card_Account_Services-Cancel_Credit_Card |
| Kundenkontonummer | #Account_Management-Account_Number_Inquiry |
| Kundenprofil | #Account_Management-Customer_Profile |
| Kundenreklamation | #Complaints-Misc |
| Kundentreueprogramm | #Account_Management-Customer_Loyalty_Program |
| Kundentreuestatus | #Account_Management-Loyalty_Status |
| Missbrauch`*` | #Account_Management-Fraudulent_Use |
| Mit Kundenbetreuer verbinden | #Help-Connect_to_Agent |
| Nächstgelegene Filiale finden`*` | #Information-Find_Nearest_Store |
| Offene Stellen | #Information-Jobs |
| Online-Kontozugriff | #Online_Account_Access-Misc |
| Online-Rechnungen | #Billing-Online_Statements |
| Papierrechnungen | #Billing-Paper_Statements |
| Profilkennwortabfrage | #Account_Management-Profile_Password |
| Profilsicherheitsfragen | #Account_Management-Profile_Security_Questions |
| Punkte einlösen | #Account_Management-Redeem_Points |
| Punkte übertragen | #Account_Management-Transfer_Points |
| Punktewert | #Account_Management-Points_Value |
| Ratenzahlung | #Payment-Installments |
| Rechnungserklärung | #Billing-Bill_Explanation |
| Rechnungskopie anfordern | #Billing-Bill_Copy |
| Rechnungskorrektur | #Billing-Request_Adjustment |
| Rechnungsreklamation | #Billing-Dispute |
| Rechnungszeitraum | #Billing-Billing_Cycle |
| Scheckbuch anfordern | #Checking_Savings_Accounts-Request_Checkbook |
| Sicherheitsgarantie | #Help-Security_Assurance |
| Standort einer Filiale`*` | #Information-Store_Location |
| Steuerformulare anfordern | #Credit_Card_Account_Services-Tax_Forms |
| Systeminformationen | #Help-Misc |
| Telefonnummer aktualisieren`*` | #Account_Management-Update_Change_Contact_Phone_Number |
| Telefonnummer einer Filiale`*` | #Information-Store_Phone_Number |
| Termin vereinbaren | #Information-Make_Appointment |
| Termin verschieben | #Information-Change_Appointment |
| Verloren gegangenen oder gestohlenen Karte melden`*` | #Credit_Card_Account_Services-Report_Lost_Or_Stolen_Card |
| Verspätungszuschlag | #Payment-Late_Fees |
| Wiederkehrende Zahlungen (autopay) | #Payment-Recurring_Payment_Autopay |
| Zahlung auschieben | #Payment-Defer_Payment |
| Zahlungen allgemein | #Payment-Misc |
| Zahlungserinnerungen | #Billing-Payment_Reminders |
| Zahlungsfälligkeitsdatum | #Payment-Payment_Due_Date |
| Zahlungsfälligkeitsdatum ändern | #Payment-Payment_Due_Date_Change |
| Zahlungsmodalitäten | #Payment-Payment_Arrangement |
| Zahlungsnachforschung | #Payment-Research_Payment |
| Zahlungsorte | #Payment-Payment_Locations |
| Zahlungsüberprüfung | #Payment-Verify_Payment |
| Zahlungsübersicht | #Payment-Payment_History |
| Zustellungsmethoden bearbeiten (E-Mail-, Apple-Benachrichtigungen) | #Alerts-Edit_Delivery_Methods |
| Öffnungszeiten`*` | #Information-Store_Hours |
| Über uns | #Information-About_Us |


`*` [Integrierte Dialoge](configure.html#builtin_dialog_ovw)

[![Zurück nach oben](images/up-arrow.png)](intent_codenames_banking.html#top)
