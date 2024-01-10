# ElecFreaks micro:bit Smart Home Kit

# Tutoriel 8

## @showdialog

Utilise les capteurs, le bouclier d'extension et les câbles.

## Étape 1

Ajoute le bloc ``||LED:activer LED||`` dans le bloc ``||basic:au démarrage||``.

La valeur ``||logic:faux||`` du bloc ``||LED:activer LED||`` demeure la même.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

led.enable(false)
basic.forever(function () {
	
})

```

## Étape 2

Ajoute le bloc ``||basic:pause (ms)||`` sous le bloc ``||LED:activer LED||``.

La valeur ``||basic: 100 ||`` du bloc ``||basic:pause (ms)||`` demeure la même.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

led.enable(false)
basic.pause(100)

```

## Étape 3

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Celcius||``.

Ajoute le bloc ``||variables: définir Pourcentage ||`` sous le bloc ``||basic: pause (ms) ||``. 

Remplace la valeur ``||variables: 0||`` par le bloc ``||smarthome: value of temperature||`` (trad: la valeur de la température).


```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

led.enable(false)
basic.pause(100)
let Celcius = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P1)
basic.forever(function () {
	
})



```

## Étape 4

Modifie le bloc ``||smarthome:  value of temperature ||``.

La valeur ``||smarthome:  celcius ||`` demeure la même.

Remplace la valeur ``||smarthome:  P1 ||`` par  ``||smarthome:  P2 ||``.


```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

led.enable(false)
basic.pause(100)
let Temps = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P2)
basic.forever(function () {
	
})

```

## Étape 5

Ajoute le bloc ``||basic: pause (ms) ||`` dans le bloc ``||basic: toujours ||``.

Remplace la valeur ``||basic: 100||`` par ``||basic: 2000||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

basic.forever(function () {
    basic.pause(2000)
})
```

## Étape 6

Ajoute le bloc ``||logic: si vrai alors sinon||`` sous le bloc ``||basic: pause (ms) ||``.


```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

basic.forever(function () {
    basic.pause(2000)
    if (true) {
    	
    } else {
    	
    }
})

```

## Étape 7

Modifie le bloc ``||logic: si vrai alors sinon||``.

Remplace la valeur ``||logic: vrai||`` par le bloc ``||logic: 0 <= 0||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

basic.forever(function () {
    basic.pause(2000)
    if (0 <= 0) {
    	
    } else {
    	
    }
})

```

## Étape 8

Modifie le bloc ``||logic: 0 <= 0||``.

Remplace la valeur ``||logic: 0||`` de gauche par le bloc ``||variables: Celcius||``.

Remplace la valeur ``||logic: 0||`` de droite par la valeur ``||logic: 25||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

basic.forever(function () {
    let Celcius = 0
    basic.pause(2000)
    if (Celcius <= 25) {
    	
    } else {
    	
    }
})


```

## Étape 9

Ajoute le bloc ``||variables:  définir strip ||`` (trad. : bande lumineuse) de l'onglet ``||neopixel:  neopixel ||`` dans le bloc ``||basic:toujours||``.

Remplace la valeur ``||neopixel:  P0 ||`` par ``||neopixel:  P1 ||``.

Remplace la valeur ``||neopixel:  24 ||`` par  ``||neopixel:  1 ||``.

La valeur ``||neopixel:  RGB ||`` demeure la même.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let strip: neopixel.Strip = null
basic.forever(function () {
    let Celcius = 0
    basic.pause(2000)
    if (Celcius <= 25) {
        strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
    } else {
    	
    }
})

```

## Étape 10

Ajoute le bloc ``||neopixel:  régler couleur||`` sous le bloc ``||variables:  définir strip ||``.

Remplace la valeur ``||neopixel: couleur||`` par la valeur ``||neopixel: noir||``. 
```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let strip: neopixel.Strip = null
basic.forever(function () {
    let Celcius = 0
    basic.pause(2000)
    if (Celcius <= 25) {
        strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
        strip.showColor(neopixel.colors(NeoPixelColors.Black))
    } else {
    	
    }
})


```

## Étape 11

Ajoute le bloc ``||variables:  définir strip ||`` (trad. : bande lumineuse) de l'onglet ``||neopixel:  neopixel ||`` sous le bloc ``||logic:sinon||``.

Remplace la valeur ``||neopixel:  P0 ||`` par ``||neopixel:  P1 ||``.

Remplace la valeur ``||neopixel:  24 ||`` par  ``||neopixel:  1 ||``.

La valeur ``||neopixel:  RGB ||`` demeure la même.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let strip: neopixel.Strip = null
basic.forever(function () {
    let Celcius = 0
    basic.pause(2000)
    if (Celcius <= 25) {
        strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
        strip.showColor(neopixel.colors(NeoPixelColors.Black))
    } else {
        strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
    }
})

```

## Étape 12

Ajoute le bloc ``||neopixel:  régler couleur||`` sous le bloc ``||variables:  définir strip ||``.

Remplace la valeur ``||neopixel: couleur||`` par la valeur ``||neopixel: rouge||``. 
```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let strip: neopixel.Strip = null
basic.forever(function () {
    let Celcius = 0
    basic.pause(2000)
    if (Celcius <= 25) {
        strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
        strip.showColor(neopixel.colors(NeoPixelColors.Black))
    } else {
        strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
        strip.showColor(neopixel.colors(NeoPixelColors.Red))
    }
})

```

## Étape 13

Voici la programmation complète du programme.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let strip: neopixel.Strip = null
led.enable(false)
basic.pause(100)
let Celcius = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P2)
basic.forever(function () {
    OLED.writeNumNewLine(Celcius)
    basic.pause(2000)
    if (Celcius <= 25) {
        strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
        strip.showColor(neopixel.colors(NeoPixelColors.Black))
    } else {
        strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
        strip.showColor(neopixel.colors(NeoPixelColors.Yellow))
    }
})


```

## @showdialog 

Félicitations! Tu as terminé la programmation. Réalise maintenant les branchements.

Dans quel port du bouclier d'extension dois-tu brancher la lumière ?

Pour tester le circuit électrique, télécharge la programmation dans le micro:bit.