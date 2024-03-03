<p align="right">Datum:18.01.2024</p>

Tags: #informatik 
---

# Algorithmen Beurteilen
#### Laufzeitbemessung
Eine Laufzeitbemessung in Millisenkunden liegt dem Problem der Vergleichbarkeit zu grunde. 
Eine Bemessung anhand von Komplexitätsklassen sichert diese.

#### Big O
von $500 + 3n + \frac{1}{3}*n^2$
O($n^2$)

#### Vergleich
1. $n^2$ und $2^n$ für 3
	1. $3^2 = 9$ und $2^3 = 8$
	2. O(n²) und O($2^n$)
	3. Die Expondetielle Laufzeit ist also für eingaben bis 3 schneller
2. $100 · log_2(n)$ und $0.0001·n^2$ für n = 100
	1. 664.38 und 1
	2. O(log(n)) und log($n^2$)
	3. Die Quadratische Laufzeit ist hier also für die eingabe 100 schneller