# Generelt om kryptering:

## Kryptering

Kryptering bruges med henblik på at kun den tiltænkte modtager kan læse det.

Det kan dog omgås med diverse tricks - som hvis man faktisk benytter en beskedtjenestes publickey (eller en delt privatekey), og den tænkte modtager gør det samme.
---

### 1. Symmetrisk (Secret Key)
* **En fælles Secret Key** til både kryptering og dekryptering.
* **Fordel:** Super hurtig.
* **Problem:** Nøglen skal deles sikkert, før man kan kommunikere. (svært, skal basically gøres fysisk.)

<img width="600" height="350" alt="image" src="https://github.com/user-attachments/assets/3b8ec2a7-4820-464f-a795-5ca372c4e54e" />

---

### 2. RSA (Asymmetrisk) (Public & Secret Key)
* Bruger nøglepar: Public Key og Secret Key.
* **Fordel:** Løser problemet med nøgledeling, fordi Secret Key ALDRIG deles.
* **Problem:** Langsommere.

<img width="600" height="350" alt="image" src="https://github.com/user-attachments/assets/8050505f-baa3-4b3b-9d8b-9e6c5edab98a" />


#### Nøgleparret
* **Public Key:** Offentlig. Bruges af alle til at **kryptere** data, som kun ejeren kan læse.
* **Secret Key:** Hemmelig. Kun **ejeren** har den. Den **eneste** der kan **dekryptere** data krypteret med den tilhørende Public Key.

#### Digital Signatur
* Bruges til at garantere **autenticitet** (hvem er afsenderen?) og **integritet** (er beskeden ændret?).
* Afsender krypterer hash af besked med **sin Secret Key**.
* Modtager tjekker signaturen med afsenders **Public Key**.

---

## Hashing (aka digitalt fingeraftryk)

Hashing =  Data laves om til en hash-værdi

* Det benyttes til at sikre integritet af data - ( altså, har dataen blevet pillet ved?).
    * Hvis en bit ændres, er hashen helt anderledes.
*  Brugses til at verificere data: Tjekke om downloadede filer er intakte.
* Ved adgangskoder: Gemmer hashen af koden i databasen, som den compare med

-------------------

.

# Krypteringsprojekt(er) eksempler

### Eksempel på client-client RSA m. python
https://github.com/Trlton/encryptionOpgaver/blob/main/encryptionOpg1.py


### Præsentation af steganografi projekt

<img width="711" height="557" alt="image" src="https://github.com/user-attachments/assets/ffd79f38-9d71-4dca-b346-d28025907c06" />


<img width="1908" height="1074" alt="image" src="https://github.com/user-attachments/assets/7fa9d7d2-a19b-4849-a71e-a246e371c37d" />


<img width="1903" height="1070" alt="image" src="https://github.com/user-attachments/assets/a42ff6ba-6290-438a-b9d9-b1f673e3db01" />

<img width="1760" height="1067" alt="image" src="https://github.com/user-attachments/assets/23ea2648-4af7-40b5-99a6-48d50f17169c" />

<img width="978" height="828" alt="image" src="https://github.com/user-attachments/assets/7bcbe8b6-7b40-4f8c-a97b-a88ccf0ee7c1" />
