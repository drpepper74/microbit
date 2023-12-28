# ElecFreaks micro:bit Smart Home Kit

# Tutoriel 5

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

Ajoute le bloc ``||variables: définir Celcius ||`` sous le bloc ``||OLED: initialize OLED ||``. 

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Celcius = 0
led.enable(false)
OLED.init(128, 64)
basic.forever(function () {
	
})

```

## Étape 4

Modifie le bloc ``||variables: définir Celcius ||``.

Remplace la valeur ``||variables: 0 ||`` du bloc  ``||variables: définir Celcius ||`` par le bloc ``||input: Température ||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Celcius = input.temperature()
led.enable(false)
OLED.init(128, 64)
basic.forever(function () {
	
})

```

## Étape 5

Ajoute le bloc ``||OLED: show string ||`` (trad. : montrer ligne) dans le bloc ``||basic: toujours ||``.

Remplace la valeur ``||OLED: " " ||`` par le bloc ``||variables: Celcius ||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

basic.forever(function () {
    let Celcius = ""
    OLED.writeStringNewLine(Celcius)
})

```

## Étape 5

Ajoute le bloc ``||basic: pause (ms) ||`` sous le bloc ``||OLED: " " ||``.

Remplace la valeur ``||basic: 100 ||`` par ``||basic: 5000 ||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

basic.forever(function () {
    let Celcius = ""
    OLED.writeStringNewLine(Celcius)
    basic.pause(5000)
})

```


## Étape 6

Voici la programmation complète du programme.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

led.enable(false)
OLED.init(128, 64)
let Celcius: string = input.temperature()
basic.forever(function () {
    OLED.writeStringNewLine(Celcius)
    basic.pause(5000)
})


```