<p align="right">Datum:9.4.2024</p>

Tags: #mathe 

---

#  Aufgaben 9.4
## **Verkettete Funktionen integrieren**

**Allgemeines Verfahren:**

1. **Identifiziere die äußere und innere Funktion:** 
    - Die äußere Funktion ist die Funktion, die die innere Funktion umschließt.
    - Die innere Funktion ist die Funktion, die in der äußeren Funktion als Argument verwendet wird.

2. **Bestimme die Ableitung der inneren Funktion:**
    - Die Ableitung der inneren Funktion wird benötigt, um die Kettenregel anzuwenden.

3. **Wende die Kettenregel an:**
    - Die Kettenregel besagt, dass die Ableitung einer verketteten Funktion gleich dem Produkt der Ableitung der äußeren Funktion und der Ableitung der inneren Funktion ist.

4. **Integriere beide Seiten der Gleichung:**
    - Integriere die linke Seite, um die Stammfunktion der verketteten Funktion zu erhalten.
    - Integriere die rechte Seite, indem du die äußere Funktion integrierst und die Ableitung der inneren Funktion als Faktor behandelst.

5. **Füge eine Integrationskonstante hinzu:**
    - Füge eine Integrationskonstante hinzu, da die Ableitung einer Konstanten gleich 0 ist.

**Formel:**

∫ f(g(x)) dx = F(g(x)) * g'(x) + C

- f(x): äußere Funktion
- g(x): innere Funktion
- F(x): Stammfunktion von f(x)
- C: Integrationskonstante

**Beispiele:**

**1.** ∫ (x^2 + 1)^3 dx

- äußere Funktion: f(x) = x^3
- innere Funktion: g(x) = x^2 + 1
- g'(x) = 2x

∫ (x^2 + 1)^3 dx = (x^2 + 1)^4 / 4 + C

**2.** ∫ e^(sin(x)) dx

- äußere Funktion: f(x) = e^x
- innere Funktion: g(x) = sin(x)
- g'(x) = cos(x)

∫ e^(sin(x)) dx = e^(sin(x)) / cos(x) + C

**3.** ∫ ln(x^2) dx

- äußere Funktion: f(x) = ln(x)
- innere Funktion: g(x) = x^2
- g'(x) = 2x

∫ ln(x^2) dx = 2x * ln(x^2) - x^2 + C

**Präsentation:**

- Schreibe die Beispiele an die Tafel.
- Erkläre das allgemeine Verfahren Schritt für Schritt.
- Berechne die Integrale der Beispiele.
- Beantworte Fragen der Zuhörer.

**Zusätzliche Ressourcen:**

- [https://de.wikipedia.org/wiki/Ableitung](https://de.wikipedia.org/wiki/Ableitung)
- [https://www.khanacademy.org/math/calculus-all-old/integration-techniques-calc](https://www.khanacademy.org/math/calculus-all-old/integration-techniques-calc)
- [https://studyflix.de/mathematik/verkettung-von-funktionen-5658](https://studyflix.de/mathematik/verkettung-von-funktionen-5658)

**Hinweis:**

- Die obigen Beispiele sind relativ einfach. Es gibt auch verkettete Funktionen, die schwieriger zu integrieren sind.
- In einigen Fällen kann es notwendig sein, andere Integrationsmethoden zu verwenden, um die Stammfunktion einer verketteten Funktion zu finden.