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
![image](https://github.com/user-attachments/assets/d4f5febc-c919-43d9-8f90-7fbcd1550469)
