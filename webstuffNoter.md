# Tools  

## Curl  
- Bruges til at lave HTTP-anmodninger fra kommandolinjen  
- Kan hente data fra web-API'er, teste endpoints, downloade filer  
Eksempel:  
  ```sh
  curl -X GET https://lego.dk/api
  ```  

## NC - NetCat / ncat
- Ligesom cat -> spytter alt tekst ud i en fil
- NetCat bruges til at forbinde til en server, så derfra bestemmer man selv hvad man vil få ud
NetCar kan lytte efter forbindelse med:
```sh
ncat -l [port f.eks 8080]
```
(-l = listen)

andre ncat commands:
```sh 
https://www.varonis.com/blog/netcat-commands
```



## Nmap  
- Netværksscanner til kortlægning af netværk og opdagelse af åbne porte  
- Anvendes til sikkerhedsanalyse og penetrationstests  
Eksempel:  
  ```sh
  nmap -sV -p 80,443 lego.dk
  ```

# Flask + SQLite  
- Flask: Letvægts Python-webframework til API'er og webapps  
- SQLite: Embedded databasesystem, godt til mindre projekter  
- Eksempel: Flask + SQLite kan bruges til en simpel CRUD-app  

# Bug Bounty & Responsible Disclosure  
- Bug Bounty: Programmer hvor virksomheder belønner sikkerhedsforskere for at finde sårbarheder  
- Responsible Disclosure: Etiske retningslinjer for at rapportere sårbarheder på en ansvarlig måde  
- CVE (Common Vulnerabilities and Exposures): Unik ID for kendte sårbarheder (fx CVE-2024-XXXX)  

# OSI Model  

## 1. Physical Layer  
- Fysiske forbindelser (kabler, signaler, radiofrekvenser)  
- Hardware som routere, switche, access points  

## 2. Data Link Layer  
- Sikrer fejlfri datatransmission mellem enheder  
- Teknologier: MAC-adresser, Ethernet, Wi-Fi (802.11)  

## 3. Network Layer  
- Ruting af pakker mellem netværk  
- Protokoller: IP, ICMP, ARP  

## 4. Transport Layer  
- Sikrer pålidelig eller upålidelig dataoverførsel  
- Protokoller: TCP (pålidelig, forbindelsesorienteret), UDP (hurtig, forbindelsesløs)  

## 5. Session Layer  
- Håndterer sessionsoprettelse, vedligeholdelse og afslutning  
- Anvendes i: SSH, NetBIOS, RPC
- ncat ligger i denne 

## 6. Presentation Layer  
- Dataformatering, kryptering og komprimering  
- Eksempler: SSL/TLS (kryptering), ASCII/EBCDIC (tekstkodning)  

## 7. Application Layer  
- Brugerinteraktion og applikationsprotokoller  
- Protokoller: HTTP, FTP, SMTP, DNS  

# SQL injection
Det handler om at der er en computer der skal læse ting
Hvis man kan få computeren til at end indtastede brugernavn er en commando
Så afvikler den det og giver tilbage / gør det du vil have den til
Det kan ødelægge en database
