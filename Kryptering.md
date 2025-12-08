# Generelt om kryptering:

## Kryptering

Kryptering bruges med henblik på at kun den tiltænkte modtager kan læse det.

Det kan dog omgås med diverse tricks - som hvis man faktisk benytter en beskedtjenestes publickey 
(eller en delt privatekey), og den tænkte modtager gør det samme.

---

### Caesar ciphering
* Shifter alle tegn en bestemt mængde
* F.eks. JEG -> KFH når beskeden shiftes med 1 tegn/bogstav

---

### Symmetrisk (delt Secret Key)
* En fælles Secret Key til både kryptering og dekryptering.
* Fordel: Super hurtig.
* Problem: Nøglen skal deles sikkert, før man kan kommunikere. (svært, skal basically gøres fysisk.)

<img width="600" height="350" alt="image" src="https://github.com/user-attachments/assets/3b8ec2a7-4820-464f-a795-5ca372c4e54e" />

---

### RSA (Asymmetrisk) (adskildt Public & Secret Key)
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


### SIGINT steganografi projekt
#### Powerpoint af projekt:
https://tstaarhustech-my.sharepoint.com/:p:/g/personal/at103238_edu_aarhustech_dk/EQLv9cnn4S9Mn6QEjC8_d0wBYA3yvY-FNqL-SZhsvVkQqw?e=5BtlZ8


#### GitHub
https://github.com/Ag-chr/SIGINT-projekt.git
