# ElecFreaks micro:bit Smart Home Kit

# Tutoriel 4

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

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Pourcentage||``.

Ajoute le bloc ``||variables: définir Pourcentage ||`` sous le bloc ``||OLED: initialize OLED ||``. 

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

led.enable(false)
OLED.init(128, 64)
let Pourcentage = 0
basic.forever(function () {
	
})

```

## Étape 4

Ajoute le bloc ``||OLED: draw loading bar ||`` (trad. : afficher une barre de progression) dans le bloc ``||basic:toujours||``.

Remplace la valeur ``||OLED: 0 ||`` du bloc ``||OLED: draw loading bar ||`` par le bloc ``||variables:Pourcentage||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

basic.forever(function () {
    let Pourcentage = 0
    OLED.drawLoading(Pourcentage)
})

```

## Étape 5

Ajoute le bloc ``||basic: pause (ms)||`` sous le bloc ``||OLED: draw loading bar ||``.

Remplace la valeur  ``||basic: 100||`` du bloc ``||basic: pause (ms)||`` par ``||basic: 1000||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

basic.forever(function () {
    let Pourcentage = 0
    OLED.drawLoading(Pourcentage)
    basic.pause(1000)
})

```

## Étape 6

Ajoute le bloc ``||variables: modifier Pourcentage ||`` dans le bloc ``||input:lorsque le bouton A est pressé||``.

Remplace la valeur ``||variables: 0 ||`` du bloc ``||variables: modifier Pourcentage ||`` par ``||variables: 5 ||``.

Ajoute le bloc ``||OLED: clear OLED ||`` sous le bloc ``||variables: modifier Pourcentage ||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Pourcentage = 0
input.onButtonPressed(Button.A, function () {
    Pourcentage += 5
    OLED.clear()
})

```

## Étape 7

Ajoute le bloc ``||variables: modifier Pourcentage ||`` dans le bloc ``||input:lorsque le bouton B est pressé||``.

Remplace la valeur ``||variables: 0 ||`` du bloc ``||variables: modifier Pourcentage ||`` par ``||variables: -5 ||``.

Ajoute le bloc ``||OLED: clear OLED ||`` sous le bloc ``||variables: modifier Pourcentage ||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Pourcentage = 0
input.onButtonPressed(Button.B, function () {
    Pourcentage += -5
    OLED.clear()
})

```

## Étape 8

Voici la programmation complète du programme.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

input.onButtonPressed(Button.A, function () {
    Pourcentage += 5
    OLED.clear()
})
input.onButtonPressed(Button.B, function () {
    Pourcentage += -5
    OLED.clear()
})
led.enable(false)
OLED.init(128, 64)
let Pourcentage = 0
basic.forever(function () {
    OLED.drawLoading(Pourcentage)
    basic.pause(1000)
})


```

## @showdialog 

Réalise le branchement ci-dessous.

![MicroSeb](https://github.com/sbergeroncp/micro-seb/blob/master/smart_home_oled.png?raw=true)


## @showdialog 

Félicitations! Tu as terminé la programmation.

Pour tester le circuit électrique, télécharge la programmation dans le micro:bit.