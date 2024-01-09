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

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

led.enable(false)
basic.pause(100)

```

## Étape 3

Ajoute le bloc ``||variables:  définir strip ||`` (trad. : bande lumineuse) de l'onglet ``||neopixel:  neopixel ||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let strip: neopixel.Strip = null
input.onButtonPressed(Button.A, function () {
    strip = neopixel.create(DigitalPin.P0, 24, NeoPixelMode.RGB)
})

```

## Étape 4

Modifie le bloc ``||variables:  définir strip ||``.

Remplace la valeur ``||neopixel:  P0 ||`` par ``||neopixel:  P1 ||``.

Remplace la valeur ``||neopixel:  24 ||`` par  ``||neopixel:  1 ||``.

La valeur ``||neopixel:  RGB ||`` demeure la même.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let strip: neopixel.Strip = null
input.onButtonPressed(Button.A, function () {
    strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
})

```

## Étape 5

Ajoute le bloc ``||neopixel:  régler couleur||`` sous le bloc ``||variables:  définir strip ||``.

Remplace la valeur ``||neopixel: couleur||`` par l'une de ton choix. (ex. : rouge)

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let strip: neopixel.Strip = null
input.onButtonPressed(Button.A, function () {
    strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
    strip.showColor(neopixel.colors(NeoPixelColors.Red))
})

```

## Étape 6

Ajoute les blocs ``||neopixel:  supprimer||`` et ``||neopixel:  montrer||`` dans le bloc ``||input:  lorsque le bouton B est pressé ||``.


```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

input.onButtonPressed(Button.B, function () {
    let strip: neopixel.Strip = null
    strip.clear()
    strip.show()
})

```

## Étape 7

Voici la programmation complète du programme.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

input.onButtonPressed(Button.A, function () {
    strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
    strip.showColor(neopixel.colors(NeoPixelColors.Red))
})
input.onButtonPressed(Button.B, function () {
    strip.clear()
    strip.show()
})
let strip: neopixel.Strip = null
led.enable(false)

```

## @showdialog 

Félicitations! Tu as terminé la programmation. Réalise maintenant les branchements.

Dans quel port du bouclier d'extension dois-tu brancher la lumière ?

Pour tester le circuit électrique, télécharge la programmation dans le micro:bit.