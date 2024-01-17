# ElecFreaks micro:bit Smart Home Kit

# Tutoriel 2

## @showdialog

Utilise l'écran OLED, les capteurs, le bouclier d'extension et les câbles.

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

Ajoute le bloc ``||variables:  définir strip ||`` (trad. : bande lumineuse) de l'onglet ``||neopixel:  neopixel ||`` dans le bloc ``||basic:toujours||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let strip: neopixel.Strip = null
basic.forever(function () {
    strip = neopixel.create(DigitalPin.P0, 24, NeoPixelMode.RGB)
})

```

## Étape 3

Modifie le bloc ``||variables:  définir strip ||`` (trad. : bande lumineuse).

Remplace la valeur ``||neopixel:  P0 ||`` par ``||neopixel:  P1 ||``.

Remplace la valeur ``||neopixel:  24 ||`` par  ``||neopixel:  1 ||``.

La valeur ``||neopixel:  RGB ||`` demeure la même.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let strip: neopixel.Strip = null
basic.forever(function () {
    strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
})


```

## Étape 4

Ajoute le bloc ``||neopixel:  régler couleur||`` sous le bloc ``||variables:  définir strip ||`` (trad. : bande lumineuse).

La valeur ``||neopixel:  rouge ||`` demeure la même.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let strip: neopixel.Strip = null
basic.forever(function () {
    strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
    strip.showColor(neopixel.colors(NeoPixelColors.Red))
})


```

## Étape 5

Ajoute le bloc ``||basic: pause (ms) ||`` sous le bloc ``||neopixel:  régler couleur ||``.

Remplace la valeur ``||basic: 100 ||`` par ``||basic: 1000 ||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let strip: neopixel.Strip = null
basic.forever(function () {
    strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
    strip.showColor(neopixel.colors(NeoPixelColors.Red))
    basic.pause(1000)
})



```

## Étape 6

Voici la programmation complète du programme.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let strip: neopixel.Strip = null
led.enable(false)
basic.forever(function () {
    strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
    strip.showColor(neopixel.colors(NeoPixelColors.Red))
    basic.pause(1000)
})


```

## @showdialog 

Attention au bloc ``||variables:  définir strip ||`` !

Assure-toi d'utiliser ``||variables:  définir strip ||`` et non ``||variables:  définir strip ||`` suivi d'un chiffre .

Exemple : ``||variables:  définir strip1 ||`` ou ``||variables:  définir strip2 ||``.

## @showdialog 

Félicitations! Tu as terminé la programmation. Réalise maintenant les branchements.

Pour tester le circuit électrique, télécharge la programmation dans le micro:bit.