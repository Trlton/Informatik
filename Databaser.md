
## Værdier
Atomare værdier:
Der er værdier man ikke kan opdele mere i:
Som f.eks. Man skal ikke have fuldt navn. Atomar er fornavn, efternavn.


## Normalformer
Undgå redundans - opdel tabeller.

# DB-Normalisering: De Vigtigste Regler

**Hovedmål:** **MINIMERE REDUNDANS** (samme data gentages) for at undgå rod og sikre god performance. Vi skal kun rette fejl ét sted!

---

### 1. Normalform

**Fokus:** Celler og gentagelser.

* **Atomare værdier:** Hver celle må kun indeholde **én** værdi.
* **Ingen gentagende grupper:** Må ikke have kolonner som f.eks. `vare_1`, `vare_2`.
* **Fix:** Split de gentagende grupper ud i en **NY TABEL** og tag den gamle primærnøgle med over som Foreign Key.

---

### 2. Normalform

**Fokus:** Nøglen (Kun relevant ved sammensat primærnøgle!).

* Skal overholde **1NF**.
* **Regel:** Alle felter, der *ikke* er en del af primærnøglen, skal afhænge af **HELE** den sammensatte nøgle.
* **Må ikke ske:** Partiel afhængighed (et felt afhænger kun af en *del* af nøglen).
* **Fix:** Split tabellen op, så du fjerner den partielle afhængighed.

---

### 3. Normalform 

**Fokus:** Felter uden for nøglen.

* Skal overholde **2NF**.
* **Regel:** Må ikke findes felter UDEN FOR primærnøglen, som er **indbyrdes afhængige** af hinanden.
* **Ingen transitive afhængigheder:** (F.eks. KundeID -> Postnummer -> By).
* **Fix:** Flyt de indbyrdes afhængige felter (som Postnummer/By-eksemplet) ud i deres **helt nye tabel**.

---

**Husk:** Det er en **balancegang**. For mange joins (pga. for høj normalisering) kan faktisk **sænke performance**!
