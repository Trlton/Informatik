
## Værdier
Atomare værdier:
Der er værdier man ikke kan opdele mere i:
Som f.eks. Man skal ikke have fuldt navn. Atomar er fornavn, efternavn.

___

## Normalformer
Undgå redundans - opdel tabeller.

Det gør det nemmere at lave maintinance / ændringer, da ting ændres alle steder ved at ændre det et sted.

### 1. Normalform

* Atomare værdier: Hver celle må kun indeholde en værdi.
* Ingen gentagende grupper: Må ikke have kolonner som f.eks. vare_1, vare_2
* Hvis gentagende grupper: Split de gentagende grupper ud i en ny tabel og tag den gamle primærnøgle med over som Foreign Key.

---

### 2. Normalform

* Skal overholde 1. normalform.
* Alle felter, der ikke er en del af primærnøglen, skal afhænge af hele den sammensatte nøgle.
* Må ikke indeholde partiel afhængighed (et felt afhænger kun af en del af nøglen).
* Hvis du har partiel afhængighed: så split tabellen op, så du fjerner den partielle afhængighed.

---

### 3. Normalform 

* Skal overholde 2. normalform
* Der må ikke findes felter UDEN FOR primærnøglen, som er indbyrdes afhængige af hinanden.
* Må ikke have Ingen transitive afhængigheder: (F.eks. KundeID -> Postnummer -> By).
* Hvis der er transitive afhængigheder: Flyt de indbyrdes afhængige felter (som Postnummer/By-eksemplet) ud i nye tabeller.

---

### Eksempel på benyttelse: 


<img width="464" height="591" alt="image" src="https://github.com/user-attachments/assets/ee4335bf-eacb-4cf7-aa57-bbfd68813f11" />




