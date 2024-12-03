<p align="right">Datum:20.11.2024</p>

Tags: #informatik 

---

# Datenbanken

#### Nr. 1
**Tabellenschema**
Online-Buchhandel(<u>username</u>, name, vorname, adresse, email, isbn, titel, autor, preis)

**Redundanz:**
Da der \<Username> als Primärschlüssel einzigartig ist, kann der Rest der Benutzerdaten in einer Benutzerdaten-Tabelle gespeichert werden und muss nicht Redundant für jeden Kauf gespeichert werden.

Gleichermaßen könnte die ISBN als Primärschlüssel zu einer Büchersortimentsdatenbank benutzt werden.

**Annomalien:**
1) Änderungs-Anomalie, die zu Inkonsistenz über verschiedene Kaufeinträge führt.
2) Lösch-Anomalie, ein Buch kann nicht ohne Löschung der zugehörigen Kundendaten erfolgen
3) Einfüge-Anomalie, ein neues Buch kann nicht ohne unnötige Infos zu Kundendaten in das Sortiment eingefügt werden

#### Nr. 2
Produktname | Größe | Preis | Reduziert
:-:|:-:|:-:|:-:
TEXT|TEXT|ZAHL|WAHRHEITSWERT

primärschlüssel(produktname)

#### Nr.3 
fahrschule(name, vorname, gebortsdatum, fahrstundenanzahl, )

 a) Prijmärschlüssel als (Name,Vorname,GB) 
 b) redundant da Lehrkäfte doppelt 
 c) Eine Lehrkraft verlässt den Job → Änderungsannomalie wenn nicht alle einträge aktualisiert werden, Löschanomalie wenn man dafür zusätzlich noch die Lernendeneinträge läschen muüsste, Einüge annomalie wenn lehrkräfte neu hinzukommen

    
#### Nr. 4
    
a) 
Jack, terrier, 3, männlihc, jauch, günther, 123523789, 42, keine 
Rudoolf, pudel, 2, weiblich, james, melissa, 1237890, 42, keine 
Sommer, dackel, 1, männlich, bäcker, kurt, 102378, 40, aspirin 

b) evtl. Lösch-Annomalie wenn ein hund sitrbt und die beseitzedaten mitgelköscht werden müssen