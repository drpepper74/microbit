# Niveau 1

# Tutoriel 4

## @showdialog

Programme le micro:bit pour qu'il affiche une image lorsqu'un bouton du micro:bit.

Programme les boutons A, B et A+B.

## Étape 1

Supprime les blocs ``||basic: au démarrage||`` et ``||basic: toujours||``.

## Étape 2

Ajoute le bloc ``|| basic: montrer LEDs ||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

Dessine une épée de Minecraft dans le bloc ``|| basic: montrer LEDs ||``.

```blocks

input.onButtonPressed(Button.A, function () {
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

Conserve ta séquence de programmation et ajoute-en une nouvelle.

Ajoute le bloc ``|| basic: montrer LEDs ||`` dans le bloc ``||input: lorsque le bouton B est pressé||``.

Dessine une armure de Minecraft dans le bloc ``|| basic: montrer LEDs ||``.

```blocks

input.onButtonPressed(Button.B, function () {
    basic.showLeds(`
        . . . . .
        . . . . .
        . . . . .
        . . . . .
        . . . . .
        `)
})

```

## Étape 4

Conserve tes séquences de programmation et ajoute-en une nouvelle.

Ajoute le bloc ``|| basic: montrer LEDs ||`` dans le bloc ``||input: lorsque le bouton A+B est pressé||``.

Dessine objet de Minecraft dans le bloc ``|| basic: montrer LEDs ||``.

```blocks

input.onButtonPressed(Button.AB, function () {
    basic.showLeds(`
        . . . . .
        . . . . .
        . . . . .
        . . . . .
        . . . . .
        `)
})

```

## Étape 5

Télécharge le programme dans le micro:bit.

Teste le programme!