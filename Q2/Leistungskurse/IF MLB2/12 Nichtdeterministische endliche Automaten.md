<p align="right">Datum:31.01.2025</p>

Tags: #informatik 

---

# Nichtdeterministische endliche Automaten

#### Aufgabe 10
1. Es ist kein detereministischer endlicher Automat, weil es für Zustand $q_0$ und $q_1$ mehrere Übergänge für den gleichen Zustand gibt.
2. ↓
	1. $q_0→q_1→q_1 → q_1  →q_2$
	2. $q_0→q_0→q_1→q_1 → q_1  →q_2$
	3.  geht nicht
	4. geht nicht
3. 
Q = \{$q_0,q_1,q_2$\}
$q_0=q_0$
$\Sigma_\epsilon^* = \{0,1,\epsilon\}$
F = \{$q_2$\}
 
$\delta=$

-|0|1|$\epsilon$|
:-:|:-:|:-:|:-:
$q_0$|\{$q_0, q_1$\}|\{$q_0$\}|\{$q_0$\}
$q_1$|\{$q_1,q_0$\}|\{$q_1,q_2$\}|\{$q_1$\}
$q_2$|\{$q_2$\}|\{$q_2$\}|\{$q_2$\}




