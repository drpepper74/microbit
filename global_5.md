# Global Goals 6

## @showdialog

Transforme le micro:bit en panneau lumineux.

Lorsque la luminosité extérieure diminue (ex. : coucher de soleil), le panneau averti les automobilistes de faire attention aux animaux.

## @showdialog

Programme le panneau lumineux.

## Étape 1

Supprime le bloc ``||basic:au démarrage||``.

Ajoute le bloc ``||logic: si vrai alors sinon||`` dans le bloc ``||basic:toujours||``.

```blocks

basic.forever(function () {
    if (true) {
    	
    } else {
    	
    }
})

```

## Étape 2

Modifie le bloc ``||logic: si vrai alors sinon ­||``.

Remplace la valeur ``||logic: vrai ­||`` par le bloc ``||logic: 0 < 0||``.

```blocks

basic.forever(function () {
    if (0 < 0) {
    	
    } else {
    	
    }
})

```

## Étape 3

Remplace la valeur ``||logic: 0 ||`` de gauche par le bloc ``||input: niveau d'intensité lumineuse||``.

Remplace la valeur ``||logic: 0 ||`` de droite par la valeur ``||logic: 100||``.

```blocks

basic.forever(function () {
    if (input.lightLevel() < 100) {
    	
    } else {
    	
    }
})


```

## Étape 4

Ajoute le bloc ``||basic:montrer LEDs||`` dans le bloc ``||logic: si alors ||``.

Dessine l'animal de ton choix.

Tu peux également choisir le bloc ``||basic:montrer l'icône||``.

```blocks

basic.forever(function () {
    if (input.lightLevel() < 100) {
        basic.showLeds(`
            . . . . .
            . # # . .
            # # # # #
            # # # # #
            # . . # .
            `)
        basic.showIcon(IconNames.Giraffe)
    } else {
    	
    }
})

```

## Étape 5

Ajoute le bloc ``||basic:effacer écran||`` dans le bloc ``||logic: sinon ||``.

```blocks

basic.forever(function () {
    if (input.lightLevel() < 100) {
        basic.showLeds(`
            . . . . .
            . # # . .
            # # # # #
            # # # # #
            # . . # .
            `)
        basic.showIcon(IconNames.Giraffe)
    } else {
        basic.clearScreen()
    }
})

```

## @showdialog

Bravo! Tu as terminé de programmer le panneau lumineux.

Télécharge le programme dans le micro:bit. Teste le programme!
