# Analyse af TELLO dronen


Antagelse:
En dude der har en app der styrer en drone


### komponenter (sensorer)
1. Kamera
2. 
------------------------
## Præsentation:

### Input fra brugeren (tastatur, museklik, berøring o.l.)

Dronen styres fra en app. I appen er der to joysticks. De aktuelle positioner af joysticksne, i forhold til hvor de er centreret normalt, sendes til Logik.
Præsentationen modtager video fra Logik. Dette præsenteres på en af menuerne i appen i 720p, op til 100 meter væk.
Præsentationen har et tegneprogram, hvori man kan tegne hvordan dronen skal bevæge sig. Dette sendes til Logik
Præsentation har blokkode side, hvor man kan programere dronen til at flyve en bestemt rute. Dette sender den til Logik



### Præsentation af grafik, tekst, billeder o.l. til brugeren
### Sende information mellem præsentationslaget og logiklaget.



## Logik:
### Foretage logiske beregninger
### Hente informationer fra præsentationslaget og på baggrund af disse hente data fra datalaget
### Lave beregninger og andre manipulationer på data fra datalaget.

Modtager fra data, og sender video (streaming af flyvetur) til præsentation.
Modtager data fra undersidekameraret, og benytter det til at stabilisere og flyve den korrekte afstand.

## Data laget: (modtager) 

Data:
### Opbevare data
### Søge i data
### Sende information til logiklaget.



