# ElecFreaks micro:bit Smart Home Kit

# Tutoriel 10

## @showdialog

Utilise l'écran OLED, les capteurs, le bouclier d'extension et les câbles.

## Étape 1

Ajoute le bloc ``||LED:activer LED||`` dans le bloc ``||basic:au démarrage||``.

La valeur ``||logic:faux||`` du bloc ``||LED:activer LED||`` demeure la même.

Certaines broches (ex. :  P3, P4, P6, etc.) sont utilisées par le micro:bit pour allumer les lumières LEDs.

Cette séquence de programmation permet de désactiver les lumières LEDs du micro:bit pour les utiliser avec le bouclier d'extension.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

led.enable(false)
basic.forever(function () {
	
})

```

## Étape 2

Ajoute le bloc ``||OLED: initialize OLED ||`` (trad. : démarrer l'écran) sous le bloc ``||LED:activer LED||``.

Les valeurs du bloc ``||OLED: initialize OLED ||`` demeurent les mêmes.

Les valeurs ``||OLED: 128 ||`` et ``||OLED: 64 ||`` sont les dimensions (en pixels) de l'écran.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

led.enable(false)
OLED.init(128, 64)
basic.forever(function () {
	
})

```

## Étape 3

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Celcius||``.

Ajoute le bloc ``||variables: définir Celcius ||`` dans le bloc ``||loops: chaque 500 ms||``.

Remplace la valeur ``||variables:0||`` par le bloc ``||smarthome:value of temperature||`` (trad. : la valeur de la température).

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Celcius = 0
loops.everyInterval(500, function () {
    Celcius = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P1)
})

```

## Étape 4

Modifie le bloc ``||smarthome:value of temperature||`` (trad. : la valeur de la température).

La valeur ``||smarthome:C||`` demeure la même.

Remplace la valeur ``||smarthome:P0||`` par ``||smarthome:P2||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Celcius = 0
loops.everyInterval(500, function () {
    Celcius = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P2)
})

```

## Étape 5

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Lumen||``.

Ajoute le bloc ``||variables: définir Lumen ||`` sous le bloc ``||variables: définir Celcius ||``.

Remplace la valeur ``||variables:0||`` par le bloc ``||smarthome:value of light intensity||`` (trad. : la valeur du niveau d'intensité lumineuse).

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Celcius = 0
let Lumen = 0
loops.everyInterval(500, function () {
    Celcius = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P2)
    Lumen = smarthome.ReadLightIntensity(AnalogPin.P1)
})

```

## Étape 6

Modifie le bloc ``||smarthome:value of light intensity||`` (trad. : la valeur du niveau d'intensité lumineuse).

Remplace la valeur ``||smarthome:P1||`` par ``||smarthome:P3||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Celcius = 0
let Lumen = 0
loops.everyInterval(500, function () {
    Celcius = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P2)
    Lumen = smarthome.ReadLightIntensity(AnalogPin.P3)
})

```

## Étape 7

Ajoute le bloc ``||logic:si vrai alors sinon||`` sous le bloc ``||variables: définir Lumen ||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Celcius = 0
let Lumen = 0
loops.everyInterval(500, function () {
    Celcius = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P2)
    Lumen = smarthome.ReadLightIntensity(AnalogPin.P3)
    if (true) {
    	
    } else {
    	
    }
})


```

## Étape 6

Modifie le bloc ``||logic:si vrai alors sinon||``.

Remplace la valeur ``||logic:vrai||`` par le bloc ``||logic: et||`` / le bloc ``||logic: ou||``. 

Choisis.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Celcius = 0
let Lumen = 0
loops.everyInterval(500, function () {
    Celcius = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P2)
    Lumen = smarthome.ReadLightIntensity(AnalogPin.P3)
    if (0 == 0 && 0 > 0) {
    	
    } else {
    	
    }
})

```

## Étape 7

Modifie le bloc ``||logic: et||`` / le bloc ``||logic: ou||``.

Remplace l'espace de gauche par le bloc ``||logic:0 > 0||``.

Remplace la valeur ``||logic:0||`` de gauche par le bloc ``||variables:Celcius||``.

Remplace la valeur ``||logic:0||`` de droite par la valeur ``||logic:25||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Celcius = 0
let Lumen = 0
loops.everyInterval(500, function () {
    Celcius = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P2)
    Lumen = smarthome.ReadLightIntensity(AnalogPin.P3)
    if (Celcius > 25 && false) {
    	
    } else {
    	
    }
})

```

## Étape 8

Modifie le bloc ``||logic: et||`` / le bloc ``||logic: ou||``.

Remplace l'espace de droite par le bloc ``||logic:0 > 0||``.

Remplace la valeur ``||logic:0||`` de gauche par le bloc ``||variables:Lumen||``.

Remplace la valeur ``||logic:0||`` de droite par la valeur ``||logic:50||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Celcius = 0
let Lumen = 0
loops.everyInterval(500, function () {
    Celcius = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P2)
    Lumen = smarthome.ReadLightIntensity(AnalogPin.P3)
    if (Celcius > 25 && Lumen > 50) {
    	
    } else {
    	
    }
})

```

## Étape 9

Ajoute le bloc ``||variables:  définir strip ||`` (trad. : bande lumineuse) de l'onglet ``||neopixel:  neopixel ||`` dans le bloc ``||logic:si alors||``.

Modifie le bloc ``||variables:  définir strip ||``.

Remplace la valeur ``||neopixel:  P0 ||`` par ``||neopixel:  P1 ||``.

Remplace la valeur ``||neopixel:  24 ||`` par  ``||neopixel:  1 ||``.

La valeur ``||neopixel:  RGB ||`` demeure la même.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Celcius = 0
let Lumen = 0
let strip: neopixel.Strip = null
loops.everyInterval(500, function () {
    Celcius = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P2)
    Lumen = smarthome.ReadLightIntensity(AnalogPin.P3)
    if (Celcius > 25 && Lumen > 50) {
        strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
    } else {
    	
    }
})

```

## Étape 10

Ajoute le bloc ``||neopixel:  régler couleur||`` sous le bloc ``||variables:  définir strip ||``.

Remplace la valeur / la couleur ``||neopixel:  rouge ||`` par la valeur / couleur de ton choix.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Celcius = 0
let Lumen = 0
let strip: neopixel.Strip = null
loops.everyInterval(500, function () {
    Celcius = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P2)
    Lumen = smarthome.ReadLightIntensity(AnalogPin.P3)
    if (Celcius > 25 && Lumen > 50) {
        strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
        strip.showColor(neopixel.colors(NeoPixelColors.Orange))
    } else {
    	
    }
})

```

## Étape 11

Ajoute le bloc ``||variables:  définir strip ||`` (trad. : bande lumineuse) de l'onglet ``||neopixel:  neopixel ||`` dans le bloc ``||logic:sinon||``.

Modifie le bloc ``||variables:  définir strip ||``.

Remplace la valeur ``||neopixel:  P0 ||`` par ``||neopixel:  P1 ||``.

Remplace la valeur ``||neopixel:  24 ||`` par  ``||neopixel:  1 ||``.

La valeur ``||neopixel:  RGB ||`` demeure la même.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Celcius = 0
let Lumen = 0
let strip: neopixel.Strip = null
loops.everyInterval(500, function () {
    Celcius = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P2)
    Lumen = smarthome.ReadLightIntensity(AnalogPin.P3)
    if (Celcius > 25 && Lumen > 50) {
        strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
        strip.showColor(neopixel.colors(NeoPixelColors.Orange))
    } else {
        strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
    }
})

```

## Étape 12

Ajoute le bloc ``||neopixel:  régler couleur||`` sous le bloc ``||variables:  définir strip ||``.

Remplace la valeur ``||neopixel:  rouge ||`` par la valeur ``||neopixel:  noir ||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Celcius = 0
let Lumen = 0
let strip: neopixel.Strip = null
loops.everyInterval(500, function () {
    Celcius = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P2)
    Lumen = smarthome.ReadLightIntensity(AnalogPin.P3)
    if (Celcius > 25 && Lumen > 50) {
        strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
        strip.showColor(neopixel.colors(NeoPixelColors.Orange))
    } else {
        strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
        strip.showColor(neopixel.colors(NeoPixelColors.Black))
    }
})

```
## Étape 15

Modifie le bloc ``||loops:chaque 500 ms||``.

Remplace la valeur ``||loops: 500 ||`` par le bloc ``||math:0 x 0||``.

Remplace la valeur ``||math:0||`` de gauche par la valeur ``||math:1000||``.

Remplace la valeur ``||math:0||`` de droite par la valeur ``||math:5||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Celcius = 0
let Lumen = 0
let strip: neopixel.Strip = null
loops.everyInterval(1000 * 5, function () {
    Celcius = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P2)
    Lumen = smarthome.ReadLightIntensity(AnalogPin.P3)
    if (Celcius > 25 && Lumen > 50) {
        strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
        strip.showColor(neopixel.colors(NeoPixelColors.Orange))
    } else {
        strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
        strip.showColor(neopixel.colors(NeoPixelColors.Black))
    }
})

```

## Étape 16

Ajoute le bloc ``||OLED: clear OLED ||`` (trad. : effacer l'écran) dans le bloc ``||input:lorsque le bouton A est pressé||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

input.onButtonPressed(Button.A, function () {
    OLED.clear()
})

```

## Étape 17

Ajoute le bloc ``||OLED: show string ||`` (trad. : montrer la ligne) sous le bloc ``||OLED: clear OLED ||`` (trad. : effacer écran).

Remplace la valeur ``||OLED: " " ||`` par le mot ``||OLED:Celcius||``. 

Ajoute le bloc ``||OLED: show number ||`` (trad. : montrer le nombre) sous le bloc ``||OLED: show string ||``.

Remplace la valeur ``||OLED: 0 ||`` par le bloc ``||variables:Celcius||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

input.onButtonPressed(Button.A, function () {
    let Celcius = 0
    OLED.clear()
    OLED.writeStringNewLine("Celcius")
    OLED.writeNumNewLine(Celcius)
})

```

## Étape 18

Ajoute le bloc ``||OLED: clear OLED ||`` (trad. : effacer l'écran) dans le bloc ``||input:lorsque le bouton B est pressé||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

input.onButtonPressed(Button.B, function () {
    OLED.clear()
})

```

## Étape 19

Ajoute le bloc ``||OLED: draw loading bar ||`` (trad. : dessiner une ligne de progression) sous le bloc ``||OLED: clear OLED ||`` (trad. : effacer écran).

Remplace la valeur ``||OLED: 0 ||`` par le bloc ``||variables:Lumen||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

input.onButtonPressed(Button.B, function () {
    let Lumen = 0
    OLED.clear()
    OLED.drawLoading(Lumen)
})

```

## Étape 20

Voici la programmation complète du programme.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

input.onButtonPressed(Button.A, function () {
    OLED.clear()
    OLED.writeStringNewLine("Celcius")
    OLED.writeNumNewLine(Celcius)
})
input.onButtonPressed(Button.B, function () {
    OLED.clear()
    OLED.drawLoading(Lumen)
})
let strip: neopixel.Strip = null
let Lumen = 0
let Celcius = 0
led.enable(false)
OLED.init(128, 64)
loops.everyInterval(1000 * 5, function () {
    Celcius = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P2)
    Lumen = smarthome.ReadLightIntensity(AnalogPin.P3)
    if (Celcius > 25 && Lumen > 50) {
        strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
        strip.showColor(neopixel.colors(NeoPixelColors.Orange))
    } else {
        strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
        strip.showColor(neopixel.colors(NeoPixelColors.Black))
    }
})



```

## @showdialog 

Félicitations! Tu as terminé la programmation. Réalise maintenant les branchements.

Pour tester le circuit électrique, télécharge la programmation dans le micro:bit.