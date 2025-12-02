# Forord
### Se evt følgende dokumenter for at se noter:
- Gates 'n stuff.md


# 26-11-2025
Denne dag havde vi 4 timer.
Dette blev brugt på at introduceres til div. gate typer, som f.eks:
- AND
- OR
- NAND

## Projektvalg
Jeg har valgt at gå efter "Spicy" niveau.
Dette inbefatter:

8 bit lommeregner som kan
- Addere
- Subtraktere
- Multiplicere
- Dividere
- Vise output i 16 bit


## Arbejde på projekt:

Jeg valgte at arbejde i Digital-Logic-Sim, da 8 bit 
lommeregner i minecraft ville være omfattende...


Først lavede jeg derfor en række gate-typer jeg skulle benytte:

### OR-gate
<img width="632" height="229" alt="image" src="https://github.com/user-attachments/assets/ef95f3d4-e9eb-4908-9c5a-14da16ab366e" />

### NOT-gate
<img width="430" height="130" alt="image" src="https://github.com/user-attachments/assets/9328d8e1-5f25-4747-bd3e-45c1ed63a716" />

### XNOR-gate

Denne gate giver 1 som output, hvis begge inputs er begge 1 eller 0.

<img width="855" height="356" alt="image" src="https://github.com/user-attachments/assets/2030b408-3d5f-4558-b848-b622eebd4762" />

### XOR-gate

Inverse af XNOR.
Altså, hvis kun en af de to inputs er 1,
så giver output 1.

<img width="749" height="333" alt="image" src="https://github.com/user-attachments/assets/afb6f87e-85a3-401a-ad7e-99850389f35f" />

### Full ADDER
Dette fungerer som 1-bit addition, men med eventuel rest der lægges oveni.
Det kan benyttes hvis man har f.eks. 8-bit addition.

<img width="857" height="387" alt="image" src="https://github.com/user-attachments/assets/d360838e-98d8-4e6d-a7f6-3fea6c85cd1a" />

_____________________________________________________________________________________________________

# 27-11-2025
Nu vil jeg bygge en 8 bit adder. Til hjælp så jeg denne video,
hvis 4-bit adder kan skaleres op til en 8-bit adder:

https://www.youtube.com/watch?v=QZwneRb-zqA

------------------------------------------------------------------------------------------------------
### 8-Bit adder
Herunder er et billede af den 8-bit adder jeg har lavet:
For at senere kunne multiplicere osv, så har jeg gjort så der er en indicator hvis d. 9'ende bit hat et 1-tal i sig.
Altså hvis der er overflod. Det er dog det maksimale overflor, så derfor 1 i 9'ende bit.

<img width="1534" height="853" alt="image" src="https://github.com/user-attachments/assets/a1c62ff1-b195-42ba-a86b-f0319e402fbe" />

------------------------------------------------------------------------------------------------------
### ALU
Idet der skal være både addition og subtraktion, så er en 8-Bit adder ikke helt nok.
Rundt om den kan man lave en ALU. Her tages der udgangspunkt i denne video:

https://www.youtube.com/watch?v=QZwneRb-zqA

I videoen viser han hvordan man kan lave en ALU med XOR gates.



#### Resultat = 0 indicator
I videoen laver han funktionelt set en NOR4 gate.
Dette gøres bare med 4 NOT-gates og 3-AND gates.
<img width="698" height="172" alt="image" src="https://github.com/user-attachments/assets/84fe13c1-5532-4d4d-a25a-c386f0d8c864" />


For at det er mindre rodet laver jeg en NOR8-gate som en subkomponent.
<img width="822" height="460" alt="image" src="https://github.com/user-attachments/assets/ef54782b-ba21-426d-bd33-0b23d51b14dc" />




#### Selve ALU'en
<img width="1220" height="920" alt="image" src="https://github.com/user-attachments/assets/2d44f67f-5c84-441d-aca7-af86a0d7a715" />

Måden hvorpå der laves subtraktion.
Den tager brug af two's complement, hvor man, ligesom en kvint cirkel i musik, har en "cirkel" mam går rundt, når man adderer tal på.

Det gør så man reelt går fra 0 til 127, hvorefter den hopper til -128 og går mod 0 (-127,...,-2,-1,0)


<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/d7079e0a-dcf9-4fa6-98f9-eebaae8f69bb" />


Herunder ses et eksempel på -127-(-128):
Her displayer den korrekt 1 som output.

Den indikerer også en overflod (carry), hv

<img width="635" height="360" alt="image" src="https://github.com/user-attachments/assets/57094905-c448-47f4-bd12-bf3794f4ab4f" />



# 2-12-2025

Efterhånden er det på tide at lave multiplikation.

Med dette tager man udgangspunkt i, at multiplikaiton bare er gentagen addition.









