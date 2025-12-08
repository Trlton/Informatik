
## Værdier
Atomare værdier:
Der er værdier man ikke kan opdele mere i:

Som f.eks. Man skal ikke have fuldt navn. Atomar er fornavn, efternavn.

___

## Normalformer
Undgå redundans - opdel tabeller.

Det gør det nemmere at lave maintinance / ændringer, da ting ændres alle steder ved at ændre det et sted.

Følgende normalformer er kort redegjort for med følgende kilde:

https://balslev.io/programmering/database/normalisering-af-databaser/

Dog ikke Boyce-Codd, som linkes til i eksemplet

### 1. Normalform

* Atomare værdier: Hver celle må kun indeholde en værdi.
* Ingen gentagende grupper: Må ikke have kolonner som f.eks. vare_1, vare_2
* Hvis gentagende grupper: split de gentagende grupper ud i en ny tabel og tag den gamle primærnøgle med over som Foreign Key.

---

### 2. Normalform

* Skal overholde 1. normalform.
* Alle felter, der ikke er en del af primærnøglen, skal afhænge af hele den sammensatte nøgle.
* Må ikke indeholde partiel afhængighed (et felt afhænger kun af en del af nøglen).
* Hvis man har partiel afhængighed: split tabellen op, så du fjerner den partielle afhængighed.

---

### 3. Normalform 

* Skal overholde 2. normalform
* Der må ikke findes felter UDEN FOR primærnøglen, som er indbyrdes afhængige af hinanden.
* Må ikke have Ingen transitive afhængigheder: (F.eks. KundeID -> Postnummer -> By).
* Hvis der er transitive afhængigheder: Flyt de indbyrdes afhængige felter (som Postnummer/By-eksemplet) ud i nye tabeller.

---

### Eksempel på benyttelse: 

Denne følgende tabel opfylder Boyce-Codd modellen:
Som kan læses om her: (jeg magtede ikke at skrive den sektion også)

https://www.geeksforgeeks.org/dbms/boyce-codd-normal-form-bcnf/ 



<img width="500" height="600" alt="image" src="https://github.com/user-attachments/assets/1c146e0a-e189-4c4e-90aa-7a89c0593e69" />


