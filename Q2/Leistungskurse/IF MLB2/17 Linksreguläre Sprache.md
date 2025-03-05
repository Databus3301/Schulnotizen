<p align="right">Datum:26.02.2025</p>

Tags: #informatik 

---

# Linksreguläre Sprache


#### Nr. 6 a)
P = {
S → 0A...9A 
A → 0B...9B 
B → 0C...9C 
C → -D
D → aE..zE
E → aF..zF
F → 0...9
}

#### Nr.6 b)

P = {
S → 0A...9A
A → aB..zB
B → aC..zC
C → -D
D → 0E...9E 
E → 0F...9F 
F → 0...9

}

#### Nr.7 a)

a, b, aa

#### Nr.7 b)
### $(a | b)^n, n\ge 1$

#### Nr.7 c)

Weil "SS" eine der beliebigen Folgen von Nicht-Terminalen und Terminalen darstellt, die abweichend von Kombinationen der Form: (NT) | T | (TN) ist.

#### Nr.7 d)

$G = \{N,T,S,P\}$
$N = \{S\}$
$T = \{a, b\}$
$P = \{$
S -> aS | bS | a | b
}

#### Nr.8 a)

S → aSb → aSSb → abaSb → ababab 
S → aSb → abSab → ababab
S → SS → SSS → ababab

#### Nr.8 b)

S → SS → aSbS → aabbS → aabbba

XX abbbba XX 

bbbaaa

S → bSa → bbSaa  → bbbaaa 


#### Nr.8 c)

gleich viele a wie b


#### Nr.9 a)

P = {
S -> (S)S | $\epsilon$
}

#### Nr.9 b)

P = {
S -> 1S1 | 0S0 | $\epsilon$ | 0 | 1
}

#### Nr.9 c)

S -> 0S1 | 1S0 | 1S1 | 0S0 | 101 | 010



