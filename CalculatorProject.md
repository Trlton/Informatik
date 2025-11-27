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


# 27-11-2025

Nu vil jeg bygge en 8 bit adder. Til hjælp så jeg denne video,
hvis 4-bit adder kan skaleres op til en 8-bit adder:

https://www.youtube.com/watch?v=QZwneRb-zqA

### 8-Bit adder
Herunder er et billede af den 8-bit adder jeg har lavet:
For at senere kunne multiplicere osv, så har jeg gjort så der er en indicator hvis d. 9'ende bit hat et 1-tal i sig.
Altså hvis der er overflod. Det er dog det maksimale overflor, så derfor 1 i 9'ende bit.

<img width="1534" height="853" alt="image" src="https://github.com/user-attachments/assets/a1c62ff1-b195-42ba-a86b-f0319e402fbe" />


### ALU
Idet der skal være både addition og subtraktion, så er en 8-Bit adder ikke helt nok.
Rundt om den kan man lave en ALU. Her tages der udgangspunkt i denne video:

https://www.youtube.com/watch?v=QZwneRb-zqA

I videoen viser han hvordan man kan lave en ALU med XOR gates.
