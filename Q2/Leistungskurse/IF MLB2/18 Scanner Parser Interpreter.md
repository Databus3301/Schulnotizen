<p align="right">Datum:19.03.2025</p>

Tags: #informatik 

---

# Scanner Parser Interpreter

#### Nummer 2
#### a)
![[Pasted image 20250319093211.png]]
> T = {#, A, B, C, 1, 2,3, 4}
> START, EBENE, FACH
1. \#A1 $\in$ $T^*$
2. \#BA3 $\in$ $T^*$
3. AB2#123BA# $\in$ $T^*$


#### b)
![[Pasted image 20250319094438.png]]

#### c)
![[Pasted image 20250319094514.png]]
1. (BEGINN, #), (EBENE, B)
2. (EBENE, A), (EBENE, B), (EBENE, A) ,(EBENE, B), (FACH, 1), (FACH, 2), (FACH, 3)
3. (BEGINN, #), (EBENE, C), (FACH, 2)


#### d)
1. \#X3
	- Für #
		- Anhängen von (BEGINN, #) zur Tokenlisten
		- Ausgeben des Tokens
	- Für X 
		- "Kein Token gefunden für X"
		- "Scanner: Diese Eingabe ist nicht lexikalisch korrekt"
2. AB4\#
	- Für A
		- Anhängen von (EBENE, A) zur Tokenlisten
		- Ausgeben des Tokens
	- Für B
		- Anhängen von (EBENE, B) zur Tokenlisten
		- Ausgeben des Tokens
	- Für 4
		- Anhängen von (FACH, 4) zur Tokenlisten
		- Ausgeben des Tokens
	- Für \#
		- Anhängen von (BEGINN, #) zur Tokenlisten
		- Ausgeben des Tokens
	- "\nScanner: Diese Eingabe ist lexikalisch Korrekt."


#### e)
![[Pasted image 20250319100429.png]]


```java

public String eingabeSaeubern(String pEingabe) {
	return pEingabe.replaceAll(" ", "");
}
```



#### Nr. 4

![[Pasted image 20250320093754.png]]



#### Nr. 6
```java
public boolean parse(String num) {
	int STATE = 0; // 0 -> +/- | 1 -> 0-9 & epislon
	for(int i = 0; i < num.length(); i++) {
		char c = num.charAt(i);
		if (STATE == 0) {
			if("+-".contains(c+ "") || Character.isDigit(c))
				STATE++;
			else
				return false;
		} else {
			if(!Character.isDigit(c))
				return false;
		}
	}
	return num.length() > 0;
}

```