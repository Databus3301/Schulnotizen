<p align="right">Datum:14.02.2025</p>

Tags: #informatik 

---

# Mealy-Automat

#### Nr.17 a)

$Q = \{q_0,q_1,q_2,q_3\}$
$q_0 = \{q_0\}$ 
$\Sigma = \{a,b\}$
$\Omega = \{0,1\}$
$\delta =$

Zustand | Eingabe | Übergang
:-:|:-:|:-:|
$q_0$|a|$q_0$
$q_0$|b|$q_1$
$q_1$|b|$q_1$
$q_1$|a|$q_2$
$q_2$|b|$q_3$
$q_2$|a|$q_0$
$q_3$|a|$q_2$
$q_3$|b|$q_1$



$\lambda =$

Zustand | a | b
:-:|:-:|:-:|
$q_0$|0|0
$q_1$|0|0
$q_2$|0|0
$q_3$|1|0


#### b)

babaa
00010

abababaabbaba
0000101000001


##### c)

"baba"