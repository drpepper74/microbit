# ElecFreaks micro:bit Smart Home Kit

# Tutoriel 3

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

Ajoute le bloc ``||OLED:draw rectangle||`` (trad: dessiner un rectangle) dans le bloc ``||basic:toujours||``.

Modifie le bloc ``||OLED: draw rectangle ||``.

Remplace les coordonnées :

x : 20
y : 20

par 

x : 122
y : 62

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

basic.forever(function () {
    OLED.drawRectangle(
    0,
    0,
    126,
    62
    )
})

```

## Étape 4

Ajoute le bloc ``||basic: pause (ms)||`` sous le bloc ``||OLED: draw rectangle ||``.

Remplace la valeur  ``||basic: 100||`` du bloc ``||basic: pause (ms)||`` par ``||basic: 5000||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

basic.forever(function () {
    OLED.drawRectangle(
    0,
    0,
    126,
    62
    )
    basic.pause(5000)
})

```

## Étape 5

Voici la programmation complète du programme.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

led.enable(false)
OLED.init(128, 64)
basic.forever(function () {
    OLED.drawRectangle(
    0,
    0,
    126,
    62
    )
    basic.pause(5000)
})

```

## @showdialog 

Réalise le branchement ci-dessous.

![MicroSeb](https://github.com/sbergeroncp/micro-seb/blob/master/smart_home_oled.png?raw=true)


## @showdialog 

Félicitations! Tu as terminé la programmation.

Pour tester le circuit électrique, télécharge la programmation dans le micro:bit.