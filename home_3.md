# ElecFreaks micro:bit Smart Home Kit

# Tutoriel 3

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

Ajoute le bloc ``||OLED: initialize OLED ||`` (trad. : démarrer l'écran) sous le bloc ``||LED:activer LED||``.

Les valeurs du bloc ``||OLED: initialize OLED ||`` demeurent les mêmes.

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

Ajoute le bloc ``||variables: définir Celcius ||`` dans le bloc ``||basic: toujours ||``.

Remplace la valeur ``||variables:0||`` par le bloc ``||smarthome:value of temperature||`` (trad. : la valeur de la température).

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Celcius = 0
basic.forever(function () {
    Celcius = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P0)
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
basic.forever(function () {
    Celcius = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P2)
})

```

## Étape 5

Ajoute le bloc ``||LED:clear OLED display||`` (trad. : effacer l'écran) sous le bloc ``||variables: définir Celcius ||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Celcius = 0
basic.forever(function () {
    Celcius = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P2)
    OLED.clear()
})

```

## Étape 6

Ajoute le bloc ``||LED:show number||`` (trad. : montrer le nombre) sous le bloc ``||LED: clear OLED display ||`` (trad. : effacer l'écran).

Remplace la valeur ``||LED:0||`` par le bloc ``||variables: Celcius ||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Celcius = 0
basic.forever(function () {
    Celcius = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P2)
    OLED.clear()
    OLED.writeNumNewLine(Celcius)
})

```

## Étape 7

Ajoute le bloc ``||basic:pause (ms)||`` sous le bloc ``||LED: show number ||`` (trad. : montrer nombre).

Remplace la valeur ``||basic:100||`` par le bloc ``||basic:1000||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Celcius = 0
basic.forever(function () {
    Celcius = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P2)
    OLED.clear()
    OLED.writeNumNewLine(Celcius)
    basic.pause(1000)
})

```

## Étape 8

Voici la programmation complète du programme.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Celcius = 0
led.enable(false)
OLED.init(128, 64)
basic.forever(function () {
    Celcius = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P2)
    OLED.clear()
    OLED.writeNumNewLine(Celcius)
    basic.pause(1000)
})

```

## @showdialog 

Félicitations! Tu as terminé la programmation. Réalise maintenant les branchements.

Dans quel port du bouclier d'extension dois-tu le capteur de température ?

Pour tester le circuit électrique, télécharge la programmation dans le micro:bit.