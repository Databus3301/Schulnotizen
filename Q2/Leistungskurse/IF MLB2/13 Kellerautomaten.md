
<p align="right">Datum:06.02.2025</p>

Tags: #informatik 

---

# Kellerautomaten Hausaufgaben
#### Nr 14 a)
![[Pasted image 20250211104410.png]]

#### b)
"abc"
"aabcc"
"aaabccc"

#### c)
- Falsch, es werden für "a" immer 2 Elemente auf den Keller gelegt nachdem eines entfernt wurde
- Falsch, bei einem Kellersymbol kann auch das Kellesymbol gelesen werden?

#### d)
Um in den zum Endzustand führenden Zustand $q_1$ zu gelangen muss ein b bei gleichzeitigem A auf dem Stack gelesen werden. Ein Übergang in $q_1$ und damit $q_2$ ohne das vorige einfügen eines "A" auf den Stack und demach der Eingabe "a" ist demnach unmöglich und schließt ein n = 0 aus.

# ->  $L(a) = \{w \in \Sigma^* | a^nbc^n; n \in \mathbb{N} \land n \gt 0 \}$