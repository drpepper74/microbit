# Global Goals 4

## @showdialog

Transforme le micro:bit filet lumineux.

Chaque fois qu'un poisson s'approche du filet, le micro:bit devient lumineux et il émet un signal sonore.

## @showdialog

Programme le filet lumineux.

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

Active toutes les LEDs.

Regarde l'indice au besoin.

```blocks

basic.forever(function () {
    if (input.lightLevel() < 100) {
        basic.showLeds(`
            # # # # #
            # # # # #
            # # # # #
            # # # # #
            # # # # #
            `)
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
            # # # # #
            # # # # #
            # # # # #
            # # # # #
            # # # # #
            `)
    } else {
        basic.clearScreen()
    }
})

```

## @showdialog

Programme le signal sonore.

## Étape 6

Ajoute le bloc ``||loops:tant que||`` sous le bloc ``||logic: sinon ||``.

```blocks

basic.forever(function () {
    if (input.lightLevel() < 100) {
        basic.showLeds(`
            # # # # #
            # # # # #
            # # # # #
            # # # # #
            # # # # #
            `)
    } else {
        basic.clearScreen()
    }
    while (false) {
    	
    }
})

```

## Étape 7

Modifie le bloc ``||loops: tant que ­||``.

Remplace la valeur ``||loops: faux ­||`` par le bloc ``||logic: 0 < 0||``.

```blocks

basic.forever(function () {
    if (input.lightLevel() < 100) {
        basic.showLeds(`
            # # # # #
            # # # # #
            # # # # #
            # # # # #
            # # # # #
            `)
    } else {
        basic.clearScreen()
    }
    while (0 < 0) {
    	
    }
})

```

## Étape 8

Remplace la valeur ``||logic: 0 ||`` de gauche par le bloc ``||input: niveau d'intensité lumineuse||``.

Remplace la valeur ``||logic: 0 ||`` de droite par la valeur ``||logic: 100||``.

```blocks

basic.forever(function () {
    if (input.lightLevel() < 100) {
        basic.showLeds(`
            # # # # #
            # # # # #
            # # # # #
            # # # # #
            # # # # #
            `)
    } else {
        basic.clearScreen()
    }
    while (input.lightLevel() < 100) {
    	
    }
})

```

## Étape 9

Ajoute le bloc ``||music: jouer ton ||`` dans le bloc ``||loops: tant que||``.

Choisis une note. 

Laisse la valeur ``||music: pendant ||`` à ``||music: 1 temps ||``.

```blocks

basic.forever(function () {
    if (input.lightLevel() < 100) {
        basic.showLeds(`
            # # # # #
            # # # # #
            # # # # #
            # # # # #
            # # # # #
            `)
    } else {
        basic.clearScreen()
    }
    while (input.lightLevel() < 100) {
        music.playTone(932, music.beat(BeatFraction.Whole))
    }
})

```

## @showdialog

Bravo! Tu as terminé de programmer le filet lumineux.

Télécharge le programme dans le micro:bit. Teste le programme!
