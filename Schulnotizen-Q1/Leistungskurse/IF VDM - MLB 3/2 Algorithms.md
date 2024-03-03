<p align="right">Datum:15.01.2024</p>

Tags: #informatik 

---

# Algorithms
Einen Misch-Algorithmus Entwickeln
## a)
#### 1. Anforderungen
Eingabe: Ein eindimensialer Karten Array von *n* Karten
Ausgabe: Ein eindimensialer Karten Array von *n* Karten der die Eingabekarten in gemischter Reihenfolge enthällt

*gemischt*: zuffällig.
Wobei n > 1

#### 2. Ausgangsproblem Visualisieren
![[Pasted image 20240115121919.png]]

#### 3. Teilprobleme Identifizieren
 - Pseudozufällige Zahl generieren
	1. I(0;n)
-  Karten Vertauschen
-  Schritt 2     n·x    mal wiederhohlen
-  Zurückgeben

#### 4. Sprachelemente
- java.utitls.Random
- for schleifen
- Array Indizieren

#### 5. Pseudocode
1. 
r1 = rndm(bis n)
r2 = rndm(bis n)

2. 
tmp = karte von r1
karte von r2 = karte von r1
karte von r1 = tmp
3.  
für i in 0..n·x
<2>

4.
return krate

## b)