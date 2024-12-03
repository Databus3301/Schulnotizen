<p align="right">Datum:29.11.2024</p>

Tags: #informatik 

---

# Relationelle Datenmodelle

#### Nr. 1


1. 

Lehrkraft

Stunden | ID 
:-:|:-:
6|MV


Unterricht

Lehrkraft | Klasse
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


#### Nr. 2

Agentur

<u>Name</u> | Ort
:-:|:-:
WDR | Köln


Bestand

Agentur | MID
:-:|:-:
WDR|3301

Model

<u>MID</u>| Name | Geschlecht | Vorname | Größe
:-:|:-:|:-:|:-:|:-:
3301|Frank|Männlich|Walter|150cm


Teilnahme

MID|Shooting_ID|Honorar
:-:|:-:|:-:
3301|a0|3000000€


Shooting

Termin|Ort|<u>ID</u>|Fotograf_ID|Produkt_ID
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