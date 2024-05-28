<p align="right">Datum:18.04.2024</p>

Tags: #informatik 

---

# Sortieralgorithmen
#### Daten
```mermaid
graph LR
A{Diana 1} --> B{Anton 2} --> C{Kevin 1} --> D{Erik 2} --> E{Chantal 1}
```


#### Alphabetisch sortiert mit Bubble sort

```mermaid
graph LR
A{Diana 1} --> B{Anton 2} --> C{Kevin 1} --> D{Erik 2} --> E{Chantal 1}
```

```mermaid
graph LR
 B{Anton 2} --> A{Diana 1} --> C{Kevin 1} --> D{Erik 2} --> E{Chantal 1}
```

```mermaid
graph LR
 B{Anton 2} --> A{Diana 1} --> C{Kevin 1} --> D{Erik 2} --> E{Chantal 1}
```

```mermaid
graph LR
 B{Anton 2} --> A{Diana 1} --> D{Erik 2}  --> C{Kevin 1} -->  E{Chantal 1}
```

```mermaid
graph LR
 B{Anton 2} --> A{Diana 1} --> D{Erik 2}  --> E{Chantal 1} --> C{Kevin 1}  
```

```mermaid
graph LR
 B{Anton 2} --> A{Diana 1} --> D{Erik 2}  --> E{Chantal 1} --> C{Kevin 1}  
```

```mermaid
graph LR
 B{Anton 2} --> A{Diana 1} --> E{Chantal 1} --> D{Erik 2}  -->  C{Kevin 1}  
```

```mermaid
graph LR
 B{Anton 2} --> E{Chantal 1} --> A{Diana 1} -->  D{Erik 2}  -->  C{Kevin 1}  
```


#### Bubble Sort nach Noten
```mermaid
graph LR
 E{Chantal 1}  --> B{Anton 2} -->  A{Diana 1} -->  D{Erik 2}  -->  C{Kevin 1}  
```

```mermaid
graph LR
 E{Chantal 1}  -->  A{Diana 1} --> B{Anton 2} --> D{Erik 2}  -->  C{Kevin 1}  
```

```mermaid
graph LR
 E{Chantal 1}  -->  A{Diana 1} --> B{Anton 2} -->  C{Kevin 1}  --> D{Erik 2}   
```

```mermaid
graph LR
 E{Chantal 1}  -->  A{Diana 1} -->  C{Kevin 1} --> B{Anton 2} --> D{Erik 2}   
```

#### Quicksort nach Noten

```mermaid
graph LR
 B{Anton 2} --> E{Chantal 1} --> A{Diana 1} -->  D{Erik 2}  -->  C{Kevin 1}  
```
Pivot: Anton 2
Lower
```mermaid
graph LR 
 E{Chantal 1} --> A{Diana 1}-->  C{Kevin 1} 
```
Higher
```mermaid
graph LR
  D{Erik 2}  
```
Pirvot: Chantal 1
Higher
```mermaid
graph LR
 A{Diana 1} -->  C{Kevin 1} 

```
Lower
\-

Merged
```mermaid
graph LR
 A{Chantal 1} --> E{Diana 1} -->  C{Kevin 1} --> F{Anton 2} --> G{Erik 2}

```


Referenzergebniss:

```mermaid
graph LR
 E{Chantal 1}  -->  A{Diana 1} -->  C{Kevin 1} --> B{Anton 2} --> D{Erik 2}   
```



#### Stabilität
Ein Algorithmus ist stabil wenn er ein auf seinen Input angewandtes Sortiertkriterium bei der Sortierung nach einem Neuen beibehält.