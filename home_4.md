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

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Progression||``.

Ajoute le bloc ``||variables: définir Progression ||`` sous le bloc ``||OLED: initialize OLED ||``. 

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

led.enable(false)
OLED.init(128, 64)
let Progression = 0
basic.forever(function () {
	
})

```

## Étape 4

Ajoute le bloc ``||loops: tant que ||`` dans le bloc ``||basic:toujours||``.

Remplace la valeur ``||logic: faux ||`` par le bloc ``||logic: 0 < 0 ||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

basic.forever(function () {
    while (0 < 0) {
    	
    }
})


```

## Étape 5

Modifie le bloc ``||logic: 0 < 0 ||``.

Remplace la valeur ``||logic:0||`` de gauche par le bloc ``||variables: Progression ||``.

Remplace la valeur ``||logic:0||`` de droite par ``||logic: 100 ||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

basic.forever(function () {
    let Progression = 0
    while (Progression < 100) {
    	
    }
})

```

## Étape 6

Ajoute le bloc ``||OLED: draw loading bar ||`` (trad. : dessiner une barre de progression) dans le bloc ``||loops: tant que ||``.

Remplace la valeur ``||loops: 0 ||`` par le bloc ``||variables: Progression ||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

basic.forever(function () {
    let Progression = 0
    while (Progression < 100) {
        OLED.drawLoading(Progression)
    }
})

```

## Étape 7

Ajoute le bloc ``||variables: modifier Pourcentage ||`` sous le bloc ``||OLED: draw loading bar ||``.

Modifie le bloc ``||variables: modifier Pourcentage ||``.

Remplace la valeur ``||variables: 0 ||`` par ``||variables: 5 ||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Progression = 0
basic.forever(function () {
    while (Progression < 100) {
        OLED.drawLoading(Progression)
        Progression += 5
    }
})

```

## Étape 8

Ajoute le bloc ``||basic: pause (ms)||`` sous le bloc ``||variables: modifier Progression ||``.

Remplace la valeur  ``||basic: 100||`` du bloc ``||basic: pause (ms)||`` par ``||basic: 1000||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Progression = 0
basic.forever(function () {
    while (Progression < 100) {
        OLED.drawLoading(Progression)
        Progression += 5
    }
})

```

## Étape 9

Ajoute le bloc ``||OLED: clear OLED||`` sous le bloc ``||loops: tant que ||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Progression = 0
basic.forever(function () {
    while (Progression < 100) {
        OLED.drawLoading(Progression)
        Progression += 5
        basic.pause(1000)
    }
    OLED.clear()
})


## Étape 10

Voici la programmation complète du programme.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Progression = 0
led.enable(false)
OLED.init(128, 64)
basic.forever(function () {
    while (Progression < 100) {
        OLED.drawLoading(Progression)
        Progression += 5
        basic.pause(1000)
    }
    OLED.clear()
})

```