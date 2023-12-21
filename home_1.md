# ElecFreaks micro:bit Smart Home Kit

# Tutoriel 1

## @showdialog

Utilise les capteurs, le bouclier d'extension et les câbles.

## Étape 1

Ajoute le bloc ``||LED:activer LED||`` dans le bloc ``||basic:au démarrage||``.

La valeur ``||logic:faux||`` du bloc ``||LED:activer LED||`` demeure inchangée.

```blocks

led.enable(false)
basic.forever(function () {
	
})

```

## Étape 2

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Temps||``.

Ajoute le bloc ``||variables: définir LED ||`` dans le bloc ``||basic: toujours||``. 

```blocks

let LED = 0
basic.forever(function () {
    LED = 0
})

```

## Étape 3

Modifie le bloc ``||variables: définir LED ||``.

Remplace la valeur ``||variables: 0 ||`` du bloc ``||variables: définir LED ||`` par le bloc ``||smarthome:value of light intensity||`` (trad: valeur de l'intensité lumineuse).

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let LED = 0
basic.forever(function () {
    LED = smarthome.ReadLightIntensity(AnalogPin.P1)
})

```

## Étape 4

Modifie le bloc ``||smarthome:value of light intensity||``.

Remplace la valeur ``||smarthome:P1||`` du bloc ``||smarthome:value of light intensity||`` par ``||smarthome:P3||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let LED = 0
basic.forever(function () {
    LED = smarthome.ReadLightIntensity(AnalogPin.P3)
})

```

## Étape 5

Ajoute le bloc ``||logic:si vrai alors||`` sous le bloc ``||variables: définir LED ||``.

Remplace la valeur ``||logic:vrai||`` par le bloc ``||logic:0 < 0||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let LED = 0
basic.forever(function () {
    LED = smarthome.ReadLightIntensity(AnalogPin.P3)
    if (0 < 0) {
    	
    }
})

```

## Étape 6

Modifie le bloc ``||logic:0 < 0||``.

Remplace la valeur ``||logic:0||`` de gauche par le bloc ``||variables: LED ||``.

Remplace la valeur ``||logic:0||`` de droite par ``||logic:50||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let LED = 0
basic.forever(function () {
    LED = smarthome.ReadLightIntensity(AnalogPin.P3)
    if (LED < 50) {
    	
    }
})

```

## Étape 7

Ajoute le bloc ``||neopixel:définir strip||`` (trad. : bande lumineuse) dans le bloc ``||logic:si vrai alors||``.

Renommer la variable ``||variables: définir strip||`` par ``||variables: Bande||``.

Remplace la valeur ``||neopixel:P0||`` par ``||neopixel:P1||``.

Remplace la valeur ``||neopixel:24||`` par ``||neopixel:1||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let LED = 0
let Bande: neopixel.Strip = null
basic.forever(function () {
    LED = smarthome.ReadLightIntensity(AnalogPin.P3)
    if (LED < 50) {
        Bande = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
    }
})

```

## Étape 8

Ajoute le bloc ``||neopixel:régler couleur||`` sous le bloc ``||variables: définir Bande||``.

Remplace la valeur ``||variables:strip||`` par ``||variables: Bande||``.

La valeur ``||neopixel: rouge||`` demeure inchangée.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let LED = 0
let Bande: neopixel.Strip = null
basic.forever(function () {
    LED = smarthome.ReadLightIntensity(AnalogPin.P3)
    if (LED < 50) {
        Bande = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
        Bande.showColor(neopixel.colors(NeoPixelColors.Red))
    }
})

```

## Étape 9

Ajoute le bloc ``||basic:pause (ms)||`` sous le bloc ``||neopixel:régler couleur||``.

Remplace la valeur ``||basic:100||`` du bloc ``||basic:pause (ms)||`` par ``||basic:500||``.


```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let LED = 0
let Bande: neopixel.Strip = null
basic.forever(function () {
    LED = smarthome.ReadLightIntensity(AnalogPin.P3)
    if (LED < 50) {
        Bande = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
        Bande.showColor(neopixel.colors(NeoPixelColors.Red))
        basic.pause(500)
    }
})

```

## Étape 10

Ajoute le bloc ``||neopixel:régler couleur||`` sous le bloc ``||basic: pause (ms)||``.

Remplace la valeur ``||variables:strip||`` par ``||variables: Bande||``.

Remplace la valeur ``||neopixel: rouge||`` par ``||neopixel: bleu||``.


```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let LED = 0
let Bande: neopixel.Strip = null
basic.forever(function () {
    LED = smarthome.ReadLightIntensity(AnalogPin.P3)
    if (LED < 50) {
        Bande = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
        Bande.showColor(neopixel.colors(NeoPixelColors.Red))
        basic.pause(500)
        Bande.showColor(neopixel.colors(NeoPixelColors.Blue))
    }
})

```

## Étape 11

Ajoute le bloc ``||basic:pause (ms)||`` sous le bloc ``||neopixel:régler couleur||``.

Remplace la valeur ``||basic:100||`` du bloc ``||basic:pause (ms)||`` par ``||basic:500||``.


```package

dstemps=github:tinkertanker/pxt-smarthome

```