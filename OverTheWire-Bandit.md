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



