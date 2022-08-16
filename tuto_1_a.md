# Niveau 1

# Tutoriel Bonus A

## @showdialog

Crée une animation d'une chauve-souris volante.

## Étape 1

Supprime les blocs ``||basic:au démarrage||`` et ``||basic:toujours||``.

## Étape 2

Ajoute le bloc ``|| basic: montrer LEDs ||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

Dessine chauve-souris dans dans le bloc ``|| basic: montrer LEDs ||``.

Regarde l'indice.

```blocks

input.onButtonPressed(Button.A, function () {
    basic.showLeds(`
        # . . . #
        # # . # .
        . # # # .
        . . # . .
        . . . . .
        `)
})


```

## Étape 3

Ajoute le bloc ``|| basic: montrer LEDs ||`` sous le bloc ``|| basic: montrer LEDs ||``.

Dessine une chauve-souris dans dans le bloc ``|| basic: montrer LEDs ||``.

Regarde l'indice.

```blocks

input.onButtonPressed(Button.A, function () {
    basic.showLeds(`
        # . . . #
        # # . # .
        . # # # .
        . . # . .
        . . . . .
        `)
    basic.showLeds(`
        . . . . .
        # # . # #
        # # # # #
        . . # . .
        . . . . .
        `)
})


```

## Étape 4

Ajoute le bloc ``|| basic: montrer LEDs ||`` sous le bloc ``|| basic: montrer LEDs ||``.

Dessine une chauve-souris dans dans le bloc ``|| basic: montrer LEDs ||``.

Regarde l'indice.

```blocks

input.onButtonPressed(Button.A, function () {
    basic.showLeds(`
        # . . . #
        # # . # .
        . # # # .
        . . # . .
        . . . . .
        `)
    basic.showLeds(`
        . . . . .
        # # . # #
        # # # # #
        . . # . .
        . . . . .
        `)
    basic.showLeds(`
        . . . . .
        . # . # .
        # # # # #
        # . # . #
        . . . . .
        `)
})

```

## Étape 5

Ajoute le bloc ``|| basic: montrer LEDs ||`` dans le bloc ``||input: lorsque le bouton B est pressé||``.

Dessine une chauve-souris dans dans le bloc ``|| basic: montrer LEDs ||``.

Regarde l'indice.

```blocks

input.onButtonPressed(Button.B, function () {
    basic.showLeds(`
        . . . . .
        . . . . .
        . # # # .
        # # . # #
        # . . . #
        `)
})

```

## Étape 6

Ajoute le bloc ``|| basic: montrer LEDs ||`` sous le bloc ``|| basic: montrer LEDs ||``.

Dessine une chauve-souris dans dans le bloc ``|| basic: montrer LEDs ||``.

Regarde l'indice.

```blocks

input.onButtonPressed(Button.B, function () {
    basic.showLeds(`
        . . . . .
        . . . . .
        . # # # .
        # # . # #
        # . . . #
        `)
    basic.showLeds(`
        . . . . .
        . . . . .
        # # # # #
        # # . # #
        . . . . .
        `)
})

```

## Étape 7

Ajoute le bloc ``|| basic: montrer LEDs ||`` sous le bloc ``|| basic: montrer LEDs ||``.

Dessine une chauve-souris dans dans le bloc ``|| basic: montrer LEDs ||``.

Regarde l'indice.

```blocks

input.onButtonPressed(Button.B, function () {
    basic.showLeds(`
        . . . . .
        . . . . .
        . # # # .
        # # . # #
        # . . . #
        `)
    basic.showLeds(`
        . . . . .
        . . . . .
        # # # # #
        # # . # #
        . . . . .
        `)
    basic.showLeds(`
        . . . . .
        # . # . #
        # # # # #
        . # . # .
        . . . . .
        `)
})

```

## Étape 8

Ajoute le bloc ``|| basic: effacer l'écran ||`` dans le bloc ``|| input: lorsque le bouton A+B est pressé ||``.


```blocks

input.onButtonPressed(Button.AB, function () {
    basic.clearScreen()
})

```

## Étape 9

Télécharge le programme dans le micro:bit.

Teste le programme!
