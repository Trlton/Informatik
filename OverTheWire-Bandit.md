## Level 0 
##### SSH Connection
Dette level handler om at connect til deres server gennem Secure Shell.
Her tilføjede jeg den ekstra feature i windows "OpenSHH Sever," for at kunne gøre netop dette.

I powershell benytede jeg følgende command:
ssh -p 2220 bandit0@bandit.labs.overthewire.org

Dog var der det problem, at når jeg så havde connectet og skulle logge in med kodeord, så kunne jeg ikke skrive længere.
Jeg har også forsøgt med PuTTY og Command, samme sker der.

Derfor tog jeg til internettet, hvor jeg fandt muligheden for at skrive passworded ind i første command: https://stackoverflow.com/questions/71438968/stuck-in-bandit-level-0-overthewire-org
sshpass -p 'bandit0' ssh bandit0@bandit.labs.overthewire.org -p 2220   
Dette var dog heller ikke løsningen.

Til sidst spurgte jeg ChatGBT, hvortil den kunne svare inputtet bare var gemt.
Efter jeg forsøgte at logge ind igen kom jeg ind:
###### Hermed er level 0 done
![image](https://github.com/user-attachments/assets/d4f5febc-c919-43d9-8f90-7fbcd1550469)



## Level 0->1
For at komme til level 1 skal et password findes.
Dette skal findes i en readme fil vi nu har access til gennem bandit0 connection.

På serveren skulle man finde indholdet af filen, hvilket kunne gøres med:
cat [fil navn] 
I dette tilfælde er det så:
cat readme

![image](https://github.com/user-attachments/assets/94fa31a1-186b-48f8-9d0c-c331cbba37aa)


#### Passworded vi kiggede efter er altså så:
ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

Dette bruger vi så tli at logge ind til bandit1, her benytter jeg PuTTY
![image](https://github.com/user-attachments/assets/6dc94fff-907f-4cb4-8f5c-f9f605df6bad)



## Level 1->2
I dette level er vi loggede på bandit1
Vi skal finde et password i en fil kaldet - located in the home directory

Vi kan buge ls commanden til at se hvilke filer der er.
Der står "-" som den eneste. Da "-" er et specielt tegn, can vi ikke bare skrive cat -.
Her er vi nød til at vise det et filnavn ved: cat ./-

Output:
![image](https://github.com/user-attachments/assets/3fbab476-af5e-4224-a013-64d1f5d31d3a)

#### Vi har altså nu vores password til næste level:
263JGJPfgU6LtdEvgfWU1XP5yac29mFx


## Level 2 -> 3

Vi benytter password fra sidste level til at logge ind på bandit2
I denne opgave skal vi locate en fil der hedder:  "spaces in the file name"

Opgaven er altså hvordan man finder en fil der har mellemrum i sig

Først forsøgte jeg cat ./spaces in this file name
Her lærte jeg dog den forsøger at finde alle filerne sepereret af mellemrum.

Herefter forsøgte jeg mig med cat "[filnavn]"
Denne omklamrelse af navnet viser det er et navn, hvilket endte med at virke.
![image](https://github.com/user-attachments/assets/98e1493d-2df6-4089-b758-54acdb16c9f1)

Jeg blev dog først sikker på dette efter jeg googlede det, da jeg skrev filnavnet forkert
de gange jeg forsøgte det samme selv.
Link til kilde: https://linuxhandbook.com/filename-spaces-linux/

Note til mig selv: vær sikker på du skriver det rigtige filnavn

#### Passworded bliver altså:
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

## Level 3 -> 4
Vi stater med at loggge ind til bandit3 med login fra 2->3 stående ovenfor.

I denne opgave skal vi åbne et directory for at finde passwordet.

Hvis vi benytter ls kan vi se der er et directory "inhere"
Ved at bruge commanden "cd" : cd inhere
kan vi ændre hvilket directory vi er i.
Herinde skal vi nu finde en fil.
Ved at bruge ls kan vi ikke se nogen, dette kan være fordi de kan gemmes med **.**[resten af filnavn]

Ved at benytte "find" kan vi se disse gemte også.
Her ser vi der er en der hedder "." og en der hedder "...Hiding-From-You"
Vi kan nu åbne "...Hiding-From-You" med: cat ./[filnavn]  - altså: cat ./...Hiding-From-You
![image](https://github.com/user-attachments/assets/45c54716-b48b-440d-8995-3195db4eae6d)

#### Vi får følgende password:
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ


## Level 4 -> 5
I denne opgave starter vi med at logge ind på bandit4

Her skal vi finde hvilken fil blandt 10 har passwordet.
Vi kunne tjekke alle individuelt, men lad os i stedet lære noget.

Vi kan benytte "file" til at tjekke hvilken type info de har.
Vi kunne også her tjekke / skrive alle filnavnene individuelt,
men i stedet kan vi benytte "file *" for at tjekke alle filer.
Dog er der problemet at alle filernes navne begynder med "-", 
som gør den tror den skal tage en kommando, særligt i det alle starter med -f[resten af navn]
Dog, ligesom med "cat", kan man skrive "file --" for at alt efter ses som navne kun.
Man kan så bruge "file -- *" for at se alle navne, her er * undtaget af hvad der ses som navne.

![image](https://github.com/user-attachments/assets/04f86d0c-c5eb-40f8-ad26-5eeb8be3ebb1)

Det bliver altså hurtigt åbenlyst vi leder efter filen "-file07", da dette er den eneste
som består af ASCII text, hvilket er det passworded også står i. Det gør "data" ikke:

![image](https://github.com/user-attachments/assets/780cfb7c-6a61-4369-b969-e432c56e9a36)

vi åbner fil 07 med "cat ./"

![image](https://github.com/user-attachments/assets/5365a863-9762-4479-8e46-54b331034aa5)

#### Passworded bliver altså:
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw



## Level 5 -> 6
Vi starter endnu en gang med at logge ind på næste level, her "bandit5"

I denne opgave skal vi også locate en fil.
Denne gang har filen følgende egenskaber:
-  human-readable
-  1033 bytes in size
-  not executable

Vi bruger først "ls"
Her kan der ses at der findes en directory "inhere"
Med "cd inhere" går vi derind.

Igen med "ls" finder vi disse filer:
![image](https://github.com/user-attachments/assets/b0a9512d-06a5-47b4-b673-9ba95964bab0)

Her benytter vi først "File *" til at finde hvilke der er "human-readable", som er kriterie 1.
Det bliver så tydeligt de alle er directories:
![image](https://github.com/user-attachments/assets/af4bb159-34e7-444d-9fc6-00a1104230ab)

Der må dog være en bedre vej at tjekke individuelt alle.
Med "find" kan vi dog se en lang liste filer under hver directory.
Her er det relevant at bide mærke i at nogle af navnene har mellemrum.

For at finde hvordan man kan udspecificere kriterier med find, var jeg dog nød
til at gå til internettet. 

https://www.geeksforgeeks.org/find-command-in-linux-with-examples/

Vi kunne bruge følgende relevante kriterier:
- "-type f" - viser kun filer (f står for filer)
- "-size 1033c" - viser kun filer med størrelsen 1033 bit (c står for bit)
- "! -executable" - viser kun filer der **ikke** er executable ("!" negerer kriteriet den skal være executable)

Det samles til kommandoen:
find -type f -size 1033c ! -executable

![image](https://github.com/user-attachments/assets/103ae835-8bd2-48ec-8d50-14170c37656f)

Dette leder os til:
Directory "mabyhere07" med dens fil ".file2"
Her kan vi bruge "cat [directory name]/"[file name]"

![image](https://github.com/user-attachments/assets/3f61c2e0-cdeb-45be-be5a-d080b7e8951f)

#### Passworded bliver altså:
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG





