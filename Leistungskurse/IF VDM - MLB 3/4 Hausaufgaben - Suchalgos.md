<p align="right">Datum:07.02.2024</p>

Tags: #informatik 

---

# Hausaufgaben - Suchalgos

#### Die Lineare Suche

#### Struktogramm

For
\----------------------------

>---- search

\----------------------------

#### Andere Datenstrukturen

Ja, alles Linear durchlaufbare kommt hier in Frage unabhängig von der Ursprungsreihenfolge (LIFO, FIFO)
→ Lists, Stacks, Queues 


#### Laufzeit
Best-Case: O(1)
Worst-Case: O(n)
Avg-Case: O(n) bzw n/2


#### Implementation
```java
int s;
int[] l;

for (int e : l) {
	if(e==l)
	System.out.println("Found")
}
```


#### Worst Case Proof

Ein Logarithmus beschreibt die Anzahl an Mulitplikationen *n* die an einer Basis *b* vollzogen werden müssen um auf einen Wert *l* zu kommen.

Unser Algorithmus läuft für die Anzahl an Divisionen *n*  die an einer Basis *2* vollzogen werden bis <sub><sup>(wir unser Element gefunden haben oder)</sup></sub> der Suchbereich 1 lang ist ausgehend von einer Basis *l*, der Listenlänge.

Jede Multiplikation die zu dem Wert eines Logarithmus beiträgt kann als Summand einer Summe *s* umgeschrieben werden

>1+1+1+1+1 = s = 5
>\==
>x⁵

Bei einem Suchbereich von 1 ist auch der Logarithmus selbigens 0: $log_2(1) = 0$

Eine Division kann also ebenso als negativer Summand beschrieben werden.


>1+1+1+1+1  -1 = s = 5-1 = 4
>\==
>x⁵ / x = x⁴