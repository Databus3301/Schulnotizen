<p align="right">Datum:20.01.2025</p>

Tags: #informatik 

---

# Automaten

#### Nr.1  Parkscheinautomat

**a+b:**

```mermaid
stateDiagram-v2
    [*] --> Bereit: Start

    Bereit --> Bezahlt : Münzeinwurf
    Bezahlt --> Bestätigt : Bestätigung
    Bezahlt --> Bezahlt : Münzeinwurf
    Bestätigt --> Ticket_Entnommen : Parkschein Entahme
    
```

**c:**
Ja, da nach der Ticketentahme die einzig nächste Möglichkeit ein erneuter Bezahlprozess ist, kann auf den Letzten Zustand verzichtet werden und stattdessen der Erste wieder eingemonnen werden.


```mermaid
stateDiagram-v2
    [*] --> Bereit: Start

    Bereit --> Bezahlt : Münzeinwurf
    Bezahlt --> Bestätigt : Bestätigung
    Bezahlt --> Bezahlt : Münzeinwurf
    Bestätigt --> Bereit : Parkschein Entahme
    
```


**d:**

```mermaid
stateDiagram-v2
	direction LR
    [*] --> Bereit: Start

    Bereit --> Bezahlt : Münzeinwurf
    Bezahlt --> Bestätigt : Bestätigung
	Bestätigt --> Bereit : Parkschein Entahme

	Bezahlt --> Bereit : Abbruch
	Bezahlt --> Bezahlt : Münzeinwurf
    Bestätigt --> Bereit : Abbruch

    
```

**e:**
Die Relevanz überträgt sich, da dieses Modell ein abstraktes ist.


#### Nr.2 Getränkeautomat


a)

Zustand | Eingabe | Übergang | Effekt
:-:|:-:|:-:|:-:
Bereit|1€|1€
Bereit|2€|2€
1€|1€|2€
1€|2€|3€
2€|1€|3€
2€|2€|2€|2€ Rückgeld
3€|Auswählen|Auwahl|Menu Wechsel
Auswahl|Wähle Limo|Limo
Auswahl|Wähle Cola|Cola
Limo | Bestätigung | Ausgabe | Gibt Limo aus
Cola | Bestätigung | Ausgabe | Gibt Cola aus
Ausgabe | Getränk Entnommen | Bereit

b)

```mermaid
stateDiagram-v2
state Bezahlen {
direction LR
Bereit --> 0.5€ : 50ct Einwurf
Bereit --> 1€ : 1€ Einwurf
Bereit --> 2€ : 2€ Einwurf

0.5€ --> 1€ : 50ct Einwurf
0.5€ --> 1.5€ : 1€ Einwurf
0.5€ --> 2.5€ : 2€ Einwurf
1€ --> 1.5€ : 50ct Einwurf

1€ --> 2€ : 1€ Einwurf
1€ --> 3€ : 2€ Einwurf

1.5€ --> 2€ : 50ct Einwurf
1.5€ --> 2.5€ : 1€ Einwurf
1.5€ --> 1.5€ : 2€ Einwurf (Rückgeld)

2.5€ --> 3€ : 50ct Einwurf
2€ --> 3€ : 1€ Einwurf
2€ --> 2€ : 2€ Einwurf (Rückgeld)

}

3€ --> 3€_Auswahl : Auswählen
2€ --> 2€_Auswahl : Auswählen

3€_Auswahl --> Cola : Wählt Cola
3€_Auswahl --> Limo : Wählt Limo

2€_Auswahl --> Wasser : Wählt Wasser

Cola --> Ausgabe : Gibt Cola aus
Limo --> Ausgabe : Gibt Limo aus
Wasser --> Ausgabe : Gibt Wasser aus

Ausgabe --> Bereit


``` 


#### Nr 3

```mermaid
stateDiagram-v2
[*] --> Ausgeschaltet : Start
Ausgeschaltet --> Einsatzbereit : Druck auf den Startknopf
Einsatzbereit --> Einsatzbereit : Produkt wird in den Einkaufswagen eingelesen <br> Preis & Name werden angezeigt 
Einsatzbereit --> Bezahlen : Wird an Terminal gehalten <br> Artikelliste wird angezeigt
Bezahlen --> Bestätigt : Einkauf wird bestätigt
Bestätigt --> Bezahlt : Wird bargeldlos Bezahlt <br> Kassenbon wird ausgegeben
Bezahlt --> Ausgeschaltet
``` 