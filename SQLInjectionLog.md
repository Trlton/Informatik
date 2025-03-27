# SQL Injection challenges

## Expected usage: 111.111.111-11
Efter 20 min har jeg ikke fundet ud af hvordan man connecter.
Jeg har forsøgt at selv at hoste, nu forsøger jeg at bruge den der laver en automatisk.

![image](https://github.com/user-attachments/assets/35e0549d-fdf5-4006-880b-28c9c9254d38)


Jeg forsøger at læse vejledningen igen...

Jeg forsøgte bare at copy URL og bruge den (inde fra gitpod.io auto opsætter) fra fanen,
efter jeg ikke kunne få url-en vist til at fungere:

![image](https://github.com/user-attachments/assets/e979d481-cde9-4ade-a263-35aa53290914)


Jeg forsøger mig med at sætte den op med VS i browser i stedte for pycharm...

okay jeg har været dum, nu fungerer det:

![image](https://github.com/user-attachments/assets/0a4c9bf6-6a84-4244-903a-42b97a8901c0)

Det fordi den aldrig faktisk havde adgang til at lave det gennem pycharm

![image](https://github.com/user-attachments/assets/b3aaf38e-db5e-4654-968b-36be763e7750)

Det lader til challengen var at åbne de 3 id's på det virtuelle inviornment.

Vi går videre til næste challenge:



## ' or '1' = '1

#### SQL Injection pub info
Denne challenge starter vi med at tilgå siden blablabla.io/challenge/[overstående]

![image](https://github.com/user-attachments/assets/9df93ea8-0b0a-44ab-9134-a3c08f3a69d4)


Forståelse af hvorfor alle users værdier blev vist:

![image](https://github.com/user-attachments/assets/335cb618-2182-4518-824c-c09dd739fb2a)

cpf indsættes som ' or '1' = '1
nu bliver "where" statementet til:
WHERE u.cpf = '' or '1' = '1'

Inputtet fra brugeren blev ikke tjekket af koden, hvilket gjorde dette input blev godtaget af programmet,
hvilket gør programmet / serveren vulnerable for SQL Injection.

![image](https://github.com/user-attachments/assets/8f995a32-c6d5-4873-8208-6aaa5ecf5f23)

Herover kan man se inputtet ikke tjekkes men benyttes direkte i challenges = get_challenges_for_candidate(cpf)


####  SQL Injection private info del



