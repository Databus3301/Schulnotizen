<p align="right">Datum:09.01.2024</p>

Tags: #informatik 

---

# Datenbanken - Normalformen

##### Carsharing
|<u>Kundenummer</u>|Name|Tel|<u>Ausleihdatum</u>|<u>Kennzeichen</u>|Hersteller|Km-Stand|Baujahr|
|---|---|---|---|---|---|---|---|
|1001|Max Müller|0123456789|2025-01-01|AB 123 CD|BMW|15000|2020|
|1002|Anna Schmidt|0987654321|2025-01-03|XY 987 ZT|Audi|30000|2018|
|1003|Peter Weber|0345678901|2025-01-05|CD 654 XY|Mercedes|5000|2023|


**Name**: partielle funktionale Abhängigkeit von *Kundennummer*
**Tel**: partielle funktionale Abhängigkeit von *Kundennummer*
**Ausleihdatum**: voll funktionale Abhängigkeit von *(Kundennummer, Kennzeichen)*
**Hersteller**: partiell funktional abhängig vom *Kennzeichen*
**KM-Stand**: partiell funktional abhängig vom *Kennzeichen*
**Baujahr**: partiell funktional abhängig vom *Kennzeichen*


|Kundenummer (PK)|Name|Tel|
|---|---|---|
|1001|Max Müller|0123456789|
|1002|Anna Schmidt|0987654321
|1003|Peter Weber|0345678901

/* ↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓

|↑Kundenummer|↑Kennzeichen|↑Ausleihdatum
|:-:|:-:|:-:
|1001|AB 123 CD|2025-01-01|
|1002|XY 987 ZT|2025-01-03|
|1003|CD 654 XY| 2025-01-05|

*/ ↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑

|Kennzeichen (PK)|Hersteller|Km-Stand|Baujahr|
|---|---|---|
|AB 123 CD|BMW|15000|2020|
|XY 987 ZT|Audi|30000|2018|
|CD 654 XY|Mercedes|5000|2023|

#### Nummer 3
**Universität**
________

|<u>Mitarbeiter_ID</u>|Name|Fachgebiet|Institut
|:-:|:-:|:-:|:-:
|123|Engels|Datenbank- und Informationssysteme| Informatik
|128 |Blömer|Codes und Kryptografie|Informatik
|115|Dietz|Stochastik|Mathematik
|234|Engels|Angewandte Mathematik|Maschinenbau
|332|Sauer|Datenbank- und Informationssystem|Informatik
|443|Soltenborn|Datenbank- und Informationssysteme|Informatik


a)
- **Allgemein**
  Keine *Redundanz*?
  -> Alles voll funktional abhängig von *Mitarbeiter_ID*

- **Unter** der **Annahme** das ein Fachgebiet eindeutig einem Institut zugeordnet werden kann:
Redundanz im Speichern des Instituts

b)
- *Transitive Abhängigkeiten* 
 Mitarbeiter_ID -> Fachgebiet -> Institut

Dritte Normalform:

|Mitarbeiter_ID|Name|↑Fachgebiet|
|:-:|:-:|:-:
|123|Engels|Datenbank- und Informationssysteme
|128 |Blömer|Codes und Kryptografie|
|115|Dietz|Stochastik|
|234|Engels|Angewandte Mathematik|
|332|Sauer|Datenbank- und Informationssystem|
|443|Soltenborn|Datenbank- und Informationssysteme|


|<u>Fachgebiet</u>|Institut
|:-:|:-:|
|Datenbank- und Informationssysteme| Informatik
|Codes und Kryptografie|Informatik
|Stochastik|Mathematik
|Angewandte Mathematik|Maschinenbau


#### Nummer 6
<u>Benutzername</u> | Adresse | <u>Warenkorb_ID</u> | Datum | ArtikelNr | Bezeichnung | Menge | Preis
:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:
pink3 |rotweg köln | 456 | 06.02.13 | 10078 <br> 22900 | Rock <br> Top | 1 <br> 2 | 19.95 <br> 14.95
blue23 | lichterweg bonn | 776 | 22.03.13 | 10088 <br> 10098 <br> 10099 | Uhr <br> Armband  <br> Socken | 1 <br>  1 <br>  5 | 89.9 <br> 12.95 <br>  4.44
↓
Verletzt die Bedigung zu Atomaren Werten (z.B. "Rock Top") 1.NF
↓

<u>Benutzername</u> | Adresse | <u>Warenkorb_ID</u> | Datum | ArtikelNr | Bezeichnung | Menge | Preis
:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:
pink3 |rotweg köln | 456 | 06.02.13 | 10078 | Rock| 1  | 19.95
pink3 |rotweg köln | 456 | 06.02.13 | 22900 |  Top |  2 |  14.95
blue23 | lichterweg bonn | 776 | 22.03.13 | 10088 | Uhr | 1  | 89.9 
blue23 | lichterweg bonn | 776 | 22.03.13 |  10098  | Armband  |   1  |  12.95
blue23 | lichterweg bonn | 776 | 22.03.13 |  10099 |  Socken |   5 |   4.44
↓
Verletzt die Bedigung zu nur voll-funktionalen Abhängigkeit (z.B Benutzername → Adresse) 2.NF
↓

<u>Benutzername</u> | Adresse
:-:|:-:
pink18 |rotweg köln 
blue28 | lichterweg bonn 
 


<u>Warenkorb_ID</u> | Datum | <u>ArtikelNr</U> | Bezeichnung | Menge | Preis
:-:|:-:|:-:|:-:|:-:|:-:
456 | 06.02.13 | 10078 | Rock| 1  | 19.95
 456 | 06.02.13 | 22900 |  Top |  2 |  14.95
 776 | 22.03.13 | 10088 | Uhr | 1  | 89.9 
 776 | 22.03.13 |  10098  | Armband  |   1  |  12.95
 776 | 22.03.13 |  10099 |  Socken |   5 |   4.44


↓
Verletz Bedigung zu keinen Transitiven Abhängigkeiten (z.B Warenkorb_ID→ArtikelNR->Bezeichnung)3. NF

<u>Benutzername</u> | Adresse
:-:|:-:
pink3 |rotweg köln 
blue23 | lichterweg bonn 


↑<u>Warenkorb_ID</u> | <u>ArtikelNr</u> | Menge 
:-:|:-:|:-:|
456 | 10078 | 1  | 
 456 | 22900 |   2 |  
 776 | 10088 |  1  | 
 776  |  10098  |    1  | 
 776 |  10099 |     5 |   
 
 <u>Warenkorb_ID</u> | Datum 
 :-:|:-:
456 | 06.02.13 | 
 776 | 22.03.13 | 


<u>ArtikelNR</u> | Preis | Bezeichnung  
:-:|:-:|:-:|
 10078 | Rock | 19.95 
  22900 |  Top |  14.95
10088 | Uhr  | 89.9 
  10098  | Armband  |  12.95
10099 |  Socken  |   4.44



#### Normalformen
1. Atomarer Werterbereich
2. Nur voll-funktionale Abhängigkeiten
3. Keine Transitiven Abhängigkeiten