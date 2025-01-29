<p align="right">Datum:13.01.2025</p>

Tags: #informatik 

---

# Anwendung

#### Fahrradstation
1. NF -> alle werte sind in einem atomarem Wertebreich
2. NF -> voll funktionale abhängigkeiten
3. NF -> keine transitiven nicht erfüllt da die Farbe eines Fahrrad über den Fahrradtyp transitiv abhängig vom Typ ist


Extra tabellen:

Typ | Farbe
:-:|:-:
Kind|grün
Damen|rot
Herren|blau

Seriennr | typ | baujahr | ↑stationsname
:-:|:-:|:-:|:-:
1234|Kind|1908|markt


Für die Zukunft sind wir nicht gewappnet weil es dann keine voll funktionale abhängigkeit in der Typ // Farbe tabelle gäbe



#### Fahrradverleih | Polizeistatistik

```sql
SELECT * 
FROM polizei p
RIGHT JOIN fahrrad f
ON p.seriennr = f.seriennr

```


```sql
SELECT * 
FROM fahrrad f
WHERE f.seriennr IN __seriennummern__

```


```java
public class Main {
	public static void main(String[] args) {
	
	}
}


public class Fahrradverleihverwaltung {
	public DatabaseConnector datenbank;
	private final String STATEMENT;
	private final String STATEMENT1;
	private final int SERIENNR = 0;
	
	public Fahrradverleihverwaltung() {
		STATEMENT = "SELECT serienr"
		+ "FROM fahrrad" 
		+ "WHERE seriennr = '";
		STATEMENT1 = "SELECT serienr"
		+ "FROM fahrrad" 
		+ "WHERE seriennr IN ";
	}

	public List<String> ermittleSeriennummern(List<String> pGestohlen) {
		List<String> fahrraeder = new List<>();
		pGestohlen.toFirst();
		while(pGestholen.hasAccess()) { 
			datenbank.executeStatement(STATEMENT + pGestohlen.getCurrent() + "'");
			QueryResult r = datenbank.getCurrentQueryResult();
			if(r.getRowCount() != 0)
				r.fahrraeder.append(r.getData[0][SERIENNR]);
			
			pGestohlen.next();
		}
		return fahrraeder;
	}









	public List<String> ermittleSeriennummernIN(List<String> pGestohlen) {
		List<String> fahrraeder = new List<>();
		StringBuilder inList = new StringBuilder("(");
		pGestohlen.toFirst();
		while(pGestholen.hasAccess()) {
			inList.append("'")
			.append(pGestohlen.getContent)
			.append("', ");
			pGestohlen.next();
		}
		inList = inList.substring(0, inList.length() - 2);
		datenbank.executeStatement(STATEMENT1 + inList + ")");
		QueryResult r = datenbank.getCurrentQueryResult();
		if(r.getRowCount() == 0)
			return new List<>();
		String data = r.getData();
		for(int i = 0; i < data.length; i++) {
			fahrraeder.append(data[i][SERIENNR]);
		}
		return fahrraeder;
	}

}


```