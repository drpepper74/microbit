# Tutoriel pour l'utilisation des néopixels
 
## Step 1
Ce tutoriel te permettra de compléter la programmation des néopixels.
Pour commencer, garde les deux blocs bleus.
 
 
## Step 2
Dans l'extension neopixel, sélectionne  ``||variable: définir||`` ``||neopixel: NeoPixel sur||`` et ajoute le au bloc ``||basic: au démarrage||``
Change la valeur du ``||pins:P0||`` à ``||pins:P1||`` et change la valeur de 24 pour 8 .
 
```package
 
neopixel=github:microsoft/pxt-neopixel
```
```blocks
let strip = neopixel.create(DigitalPin.P1, 8, NeoPixelMode.RGB)
basic.forever(function () {
  
})
```
