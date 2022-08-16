# Niveau 1

# Tutoriel Bonus B

## @showdialog

Crée une animation d'un athlète. 

Utilise le bloc fonction.

## Étape 1

Supprime les blocs ``||basic:au démarrage||`` et ``||basic:toujours||``.

## Étape 2

Crée une fonction et donne-lui le nom ``||functions:jumpingjack1||``.

## Étape 3

Ajoute les blocs ``||basic:montrer LEDs||`` dans le bloc ``||functions:jumpingjack1||``.

Regarde l'indice.

```blocks

function jumpingjack1 () {
    basic.showLeds(`
        # . # . #
        . # # # .
        . . # . .
        . # . # .
        # . . . #
        `)
    basic.showLeds(`
        . . # . .
        # # # # #
        . . # . .
        . # . # .
        # . . . #
        `)
    basic.showLeds(`
        . . # . .
        . # # # .
        . # # # .
        . # . # .
        # . . . #
        `)
}


```

## Étape 4

Crée une fonction et donne-lui le nom ``||functions:jumpingjack2||``.

## Étape 5

Ajoute les blocs ``||basic:montrer LEDs||`` dans le bloc ``||functions:jumpingjack2||``.

Regarde l'indice.

```blocks

function jumpingjack2 () {
    basic.showLeds(`
        . . # . .
        . # # # .
        . # # # .
        . # . # .
        # . . . #
        `)
    basic.showLeds(`
        . . # . .
        . # # # .
        # . # . #
        . # . # .
        # . . . #
        `)
    basic.showLeds(`
        . . # . .
        # # # # #
        . . # . .
        . # . # .
        # . . . #
        `)
}

```

## Étape 6

Ajoute le bloc ``||loops:répéter 4 fois||`` dans le bloc ``||input:lorsque le bouton A est pressé||``.

Regarde l'indice.

```blocks

input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 4; index++) {
    	
    }
})

```

## Étape 7

Ajoute le bloc ``||functions:appel jumpingjack1||`` dans le bloc ``||loops:répéter 4 fois||``.

Regarde l'indice.

```blocks

function jumpingjack1 () {
    basic.showLeds(`
        # . # . #
        . # # # .
        . . # . .
        . # . # .
        # . . . #
        `)
    basic.showLeds(`
        . . # . .
        # # # # #
        . . # . .
        . # . # .
        # . . . #
        `)
    basic.showLeds(`
        . . # . .
        . # # # .
        . # # # .
        . # . # .
        # . . . #
        `)
}
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 4; index++) {
        jumpingjack1()
    }
})

```

## Étape 8

Ajoute le bloc ``||functions:appel jumpingjack2||`` sous le bloc le bloc ``||functions:appel jumpingjack1||``.

```blocks

function jumpingjack1 () {
    basic.showLeds(`
        # . # . #
        . # # # .
        . . # . .
        . # . # .
        # . . . #
        `)
    basic.showLeds(`
        . . # . .
        # # # # #
        . . # . .
        . # . # .
        # . . . #
        `)
    basic.showLeds(`
        . . # . .
        . # # # .
        . # # # .
        . # . # .
        # . . . #
        `)
}
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 4; index++) {
        jumpingjack1()
        jumpingjack2()
    }
})
function jumpingjack2 () {
    basic.showLeds(`
        . . # . .
        . # # # .
        . # # # .
        . # . # .
        # . . . #
        `)
    basic.showLeds(`
        . . # . .
        . # # # .
        # . # . #
        . # . # .
        # . . . #
        `)
    basic.showLeds(`
        . . # . .
        # # # # #
        . . # . .
        . # . # .
        # . . . #
        `)
}


```

## Étape 9

Ajoute le bloc ``|| basic: effacer l'écran ||`` dans le bloc ``|| input: lorsque le bouton B est pressé ||``.


```blocks

input.onButtonPressed(Button.B, function () {
    basic.clearScreen()
})

```

## Étape 10

Télécharge le programme dans le micro:bit.

Teste le programme!