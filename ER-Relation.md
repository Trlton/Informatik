# Entitet relation

<img width="883" height="843" alt="image" src="https://github.com/user-attachments/assets/1fc8eeb6-3558-422f-8bb1-a9a43756162e" />

# E/R 

* Det er **planen**. En tegning af din database, FØR du bygger den.
* Sikrer at strukturen er gennemtænkt og ikke tilfældig.

## Entiteter 
* De primære **objekter** systemet arbejder med (f.eks. Bruger, Produkt, Bestilling).
* **Attributter:** Egenskaber/datafelter tilknyttet entiteten.
    * Her identificeres **nøgler** (ID'er) og alm. datafelter.

## Relationer 

* Forbinder entiteterne og viser sammenhængen.
* Har kardinaliteter (hvor mange relaterer til hvor mange?).

### Kardinalitet

* **1 til 1:** En til En (F.eks. Bruger til Login-info).
* **1 til Mange:** En til M (F.eks. Kunde til Bestillinger).
* **Mange til Mange (M:M):** M til M (F.eks. Studerende til Fag).

## Resultat

E/R diagrammet giver det færdige overblik over:

1.  Hvilke **tabeller** vi skal lave.
2.  Hvilke **nøgler** (PK/FK) der skal bruges.
3.  Hvordan data skal **join'es** senere.


## Eksempel på benyttesle:

**Dette er et rough sketch, som ikke er færdiggjort. Man kan primært se kardinalitet, relationer og entiteter (altså ikke atributter)**


<img width="463" height="501" alt="image" src="https://github.com/user-attachments/assets/fc23c957-f782-47f5-9d80-0fa012cc26d5" />
