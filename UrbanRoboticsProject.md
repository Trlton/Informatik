# Links til project-stuff

Trello: https://trello.com/b/CZcmrlB5/robotics-thingy

Github: https://github.com/Fredehjort/UrbanRobotics-HTX-AFR/tree/main

MiroBoard: https://miro.com/app/board/uXjVGTnhFJA=/?share_link_id=194963977682

_______________________


# Project intro
Dette projekt handler om, hvordan man kan få en autonom robot til at accepteres nemmere i bybilledet.

_______________________


## Valg af retning

Ud fra dette ide-træ er der valgt noget:
https://miro.com/app/board/uXjVGTnhFJA=/?share_link_id=236039784756

<img width="1267" height="681" alt="image" src="https://github.com/user-attachments/assets/942363d9-2c7f-49d9-a25f-95bb04715f67" />


Vi har valgt at arbejde med at, ud fra hvad den autonome robot oplever, den vil den reagere audiativt og visuelt på stimuli.
Dette kan f.eks. være at den kører fremad/bagud, rystes, venter på at køre over et kryds osv.

Her vælges det at benytte en højtaler og LCD skærme.
LCD skærmen er til at display et ansigt og to øjne.

_______________________

## Workshop m. komunen

Denne dag skulle vi finde aktører der kunne påvirkes af teknologien, eller som på nogen måde har en, ja, del i det.

Her blev der fundet frem til:
- Handikap (syns, lydmæssigt, lydsensitive osv)
- Personer i bybilledet generelt
- Gadebutiksejere (kan forstyrre deres kunder evt.)
- Robotfirma der skal købe dele er servicere de autonome robotter, evt også holde opsyn med dem
- Komune og stat ift lovgivning og mulighed for at teste robotterne (samt eventuelle klager)

_______________________

## User stories

<img width="640" height="250" alt="image" src="https://github.com/user-attachments/assets/3a83da46-8e02-4457-a661-870e08688441" />


_______________________

## Ideer til scenarier den kan reagere på:

Holde stille
- Vente ved rødt lys

Køre fremad
- Dreje retning

Køre bagud
- Dreje retning

Oplever ryst

Væltet
_______________________

## Ideer til komponenter

1) Arduinno
2) ESP32
3) LCD display
4) Højtaler
5) Accelerometer

## Valgte komponenter
-	I2S Audio Breakout
-	Speaker
-	D1mini32+grove Shield
-	Grove-LCD RGB Backlight
-	6-axis gyroscope and accelerometer BMI088 v1.1
_______________________

## 3-lags-model af Arli-robot


<img width="1141" height="622" alt="image" src="https://github.com/user-attachments/assets/3e5c40a2-bb87-4d50-bb30-1d72f9c2b5c2" />

Her er der en ny måde jeg fortolker hvordan man kan lave 3-lags-modeller, som er mindre flowchart agtige.

_______________________

## 3-lags-model af udarbejdet løsning
Iteration 2

<img width="795" height="553" alt="image" src="https://github.com/user-attachments/assets/7048c8bc-36ec-46a9-bdab-5f1e13a5fd21" />

_______________________

## Flowchart over tænkt løsning - iteration 1 (kinda 4)

<img width="452" height="912" alt="image" src="https://github.com/user-attachments/assets/23e3c385-63b9-4ff3-a921-7d4afee179ef" />

_______________________


## Flowchart over faktisk løsning 

<img width="450" height="550" alt="image" src="https://github.com/user-attachments/assets/300e4297-41f8-40b7-9108-a011d9fb0a19" />

_______________________

## Casing til elektronik (løsning) - iteration 1
<img width="305" height="260" alt="image" src="https://github.com/user-attachments/assets/066fc15e-f46f-4309-a608-3a401dc56e38" />
<img width="277" height="286" alt="image" src="https://github.com/user-attachments/assets/4291f541-a74d-4b65-a510-fffcd9da6355" />
<img width="277" height="266" alt="image" src="https://github.com/user-attachments/assets/c19c7163-90d1-484e-93d5-4076dd6a0d60" />

_______________________

## Usaibility Heuristics påvirkning på designet


<img width="900" height="400" alt="image" src="https://github.com/user-attachments/assets/d273d858-acf9-4827-8dee-8a752ad44dce" />


<img width="900" height="600" alt="image" src="https://github.com/user-attachments/assets/daec0b3e-d846-4ce3-8aac-016535936a9e" />

