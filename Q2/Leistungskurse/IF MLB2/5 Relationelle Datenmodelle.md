<p align="right">Datum:29.11.2024</p>

Tags: #informatik 

---

# Relationelle Datenmodelle

#### Nr. 5 a)


1. 

Lehrkraft

Stunden | ID 
:-:|:-:
6|MV


Unterricht

↑Lehrkraft | ↑Klasse
:-:|:-:
MV | 6a

Klasse

Stunden | ID
:-:|:-:
24 | 6a


2. 

Mitglied

Name|ID
:-:|:-:
Jhon|42


Gym

Mitglied | Sportkurs
:-:|:-:
42|13fe56


Sportkurs

Name | ID
:-:|:-:
Yoga| 13fe56


3. 

Mitarbeitende

Name | ID | Leitung_von_Abteilungs_ID
:-:|:-:|:-:
Jochen| 123675 | qwet

Arbeitsaufteilung

Mitarbeitende|Abteilung
:-:|:-:
123675|qwet


Abteilung 

Name | ID
:-:|:-:
Prod| qwet

#### Nr. 5 b)

Verlag(Name, Ansprechpartner, Sitz, <u>VID</u>)
↓
Buch(<u>ISBN</u>, Autor, Titel, Kategorie, Preis, ↑VID)
↓
Darstellung(lieferbar, Bewertung, ↑ISBN)

Kunde(Name, Vorname, Adresse, Passwort, E-Mail, <u>Benutzername</u>)
↓
Bestellungen(Anzahl, Datum, ↑Benutzername, ↑ISBN, <u>Bestellnummer</u>)



#### Nr. 6

Agentur

<u>Name</u> | Ort
:-:|:-:
WDR | Köln

Model

<u>MID</u>| Name | Geschlecht | Vorname | Größe | ↑Agentur
:-:|:-:|:-:|:-:|:-:|:-:
3301|Frank|Männlich|Walter|150cm|WDR


Teilnahme

↑MID|↑Shooting_ID|Honorar
:-:|:-:|:-:
3301|a0|3000000€


Shooting

Termin|Ort|<u>ID</u>|↑Fotograf_ID|↑Produkt_ID
:-:|:-:|:-:|:-:|:-:
Morgen| Bochum|a0|007|.-.,


Fotograf

Name|Kamera|<u>ID</u>
:-:|:-:|:-:
Jhonathan|Sona A7 r III| 007


Produkt

Bezeichnung | Hersteller | <u>ID</u>
:-:|:-:|:-:
ShampooMAX | Bosch | .-.,


#### Nr. 7 

a)
![[Pasted image 20241205095139.png]]

b)

Firma(<u>Name</u>, Ansprechpartner)

Produkt(<u>PID</u>, Name, Kategorie, Brennwert)

Test(↑PID, ↑ID)

Produkttester(<u>ID</u>, Name, Vorname, Kategorie, Gehalt, ↑Firmen_Name)

c)
Für Löschungen auf Produkt oder Produkttester:
ON DELETE CASCADE.
