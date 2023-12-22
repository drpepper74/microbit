# ElecFreaks micro:bit Smart Home Kit

# Tutoriel 2

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

Ajoute le bloc ``||OLED: clear OLED ||`` (trad. : effacer l'écran) dans le bloc ``||basic:toujours||``.

Ajoute le bloc ``||OLED: draw line ||`` (trad. : dessiner une ligne) sous le bloc ``||OLED: clear OLED ||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

basic.forever(function () {
    OLED.clear()
    OLED.drawLine(
    0,
    0,
    0,
    0,
    )
})

```

## Étape 4

Modifie le bloc ``||OLED: draw line ||``.

Remplace les ``||OLED: coordonnées ||`` par celles-ci :

x : 0 
y : 0

to

x : 128
y : 64


```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

basic.forever(function () {
    OLED.clear()
    OLED.drawLine(
    0,
    0,
    128,
    64
    )
})

```

## Étape 5

Ajoute le bloc ``||basic: pause (ms)||`` sous le bloc ``||OLED: draw line ||``.

Remplace la valeur  ``||basic: 100||`` du bloc ``||basic: pause (ms)||`` par ``||basic: 5000||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

basic.forever(function () {
    OLED.clear()
    OLED.drawLine(
    0,
    0,
    128,
    64
    )
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
basic.forever(function () {
    OLED.clear()
    OLED.drawLine(
    0,
    0,
    128,
    64
    )
    basic.pause(5000)
})


```