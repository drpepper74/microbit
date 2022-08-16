# Niveau 1

# Tutoriel 3

## @showdialog

Programme le micro:bit pour qu'il affiche un dessin.

## Étape 1

Supprime le bloc ``||basic:au démarrage||``.

## Étape 2

Ajoute le bloc ``|| basic: montrer LEDs ||`` dans le bloc ``||basic: toujours||``.

Dessine une image dans le bloc ``|| basic: montrer LEDs ||``.

```blocks

basic.forever(function () {
    basic.showLeds(`
        . . . . .
        . . . . .
        . . . . .
        . . . . .
        . . . . .
        `)
})

```

## Étape 3

Télécharge le programme dans le micro:bit.

Teste le programme!