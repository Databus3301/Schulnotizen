<p align="right">Datum:27.11.2024</p>

Tags: #informatik 

---

# Kardinalitäten
#### Nr. 1
Mutter – 1 – hat – n – Kind

Lieferant – m – liefert – n – Artikeln
.                |
.               Anzahl

Schüler – 1 – ist Kurssprecher – n – Kurs
     |m                               /
    nimmt       teil        an    –         n      

Lehrkraft – m – unterichtet – n – Klasse
.                    |n
 .                  Fach

Person – 1 – hat – 1 – Personalausweis


Tanzkursteilnehmer – 1
.      |                \\
.     1        –        tanzt mit


#### Nr. 2
a)
Eine **Person** wird eindeutig über Name und Vorname indentifziert
Eine **Person** kann eine **Wohnung** mieten und
mehrere **Personen** können in einer **Wohnung** leben.
Eine **Wohnung** wird über eine Nummer identifziert und kann einem **Mietshaus** zugeordnet werden.
Ein **Mietshaus** hat mehrere **Wohnungen**.


#### Nr. 3


fitnesstudio(<u>Name, Adresse</u>, Gewicht, Köpergrße, 
.            Geschlecht, Körperliche Beschwerdem, KursNr, Trainingsplan)


Kunde – n – nehmen teil an – m – Kurs
. |
. 1 – hat – 1 – Chipkarte

- Kunde 
	- Name
	- Adresse
	- Gewicht
	- Körpergröße
	- Geschlecht
	- Körperliche Bescherden
	- -
	- Abo 
	- Kunden Nr.
- Kurs
	- Kurn Nr.
	- -
	- Kurs Name
	- Kurs Inhalt

- Chipkarte – 1 – ruft ab – n Trainingsplan


![[Pasted image 20241128093453.png]]


#### Nr. 4

Es ist sinnvoller für den Trainer eine eigene Entitätsmenge anzulegen, da dieser Trainer mit noch mehr daten als dem bloßen name oder so in verbindung gebracht wird und der trainerstab sich unabhängig von den mannschaften entwickeln kann.


Die Trikotnummer ist spezifisch für einen Spieler und bietet keine möglichkeit für Annomalien, also sollte sie als Attribut des Spielers Speichern