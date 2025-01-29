<p align="right">Datum:17.01.2025</p>

Tags: #informatik 

---

# SQL-Java Abi-Übung

#### Bahnlinienabfragen
1. 
```sql
SELECT Name, sum(Fahrzeit)
FROM gehoertZu gz
JOIN Bahnlinie b
ON gz.BahnlinieID = b.ID
GROUP BY b.Name
``` 
2.
```sql
SELECT gz.BahnlinieID. st.vonBahnhofName, st.zuBahnhofName
FROM gehoertZu gz
JOIN Streckenabschnitt st
ON gz.StreckenabschnittID = st.ID
WHERE gz.Fahrzeit = SELECT(max(gz.Fahrzeit) FROM gehoertZu gz);

``` 