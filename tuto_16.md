# Niveau 4

# Tutoriel 16

## @showdialog

Transforme le micro:bit en chronomètre.

## Étape 1

Supprime les blocs ``||basic: au démarrage||`` et ``||basic: toujours||``.

## Étape 2

Ajoute le bloc ``||input: lorsque le bouton A est pressé||``.

```blocks

input.onButtonPressed(Button.A, function () {
	
})

```

## Étape 3

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Chrono||``.

Ajoute le bloc ``||variables: définir Chrono à "0"||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

```blocks

let Chrono = 0
input.onButtonPressed(Button.A, function () {
    Chrono = 0
})

```

## Étape 4

Remplace la valeur ``||variables:0||`` du bloc ``||variables:définir Chrono à||`` par le bloc ``||input: temps d'exécution||``.

Ajoute le bloc ``||variables: définir Chrono à "0"||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

```blocks

let Chrono = 0
input.onButtonPressed(Button.A, function () {
    Chrono = input.runningTime()
})

```

## Étape 5

Ajoute le bloc ``||input: lorsque le bouton B est pressé||``.

```blocks

input.onButtonPressed(Button.B, function () {
	
})

```

## Étape 6

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Durée||``.

Ajoute le bloc ``||variables: définir Durée à "0"||`` dans le bloc ``||input: lorsque le bouton B est pressé||``.

```blocks

let Durée = 0
input.onButtonPressed(Button.B, function () {
    Durée = 0
})

```

## Étape 7

Remplace la valeur  ``||variables:0||`` du bloc ``||variables: définir Durée à ||`` par le bloc ``||math: 0 - 0||``.

```blocks

let Durée = 0
input.onButtonPressed(Button.B, function () {
    Durée = 0 - 0
})

```

## Étape 8

Remplace la valeur  ``||math: 0||`` de gauche par le bloc ``||input: temps d'exécution (ms)||`` dans le bloc ``||math: 0 - 0||``.

Remplace la valeur  ``||math: 0||`` de droite par le bloc ``||variables: Chrono||`` dans le bloc ``||math: 0 - 0||``.

```blocks

let Durée = 0
input.onButtonPressed(Button.B, function () {
    let Chrono = 0
    Durée = input.runningTime() - Chrono
})

```

## Étape 9

Ajoute le bloc ``||basic: afficher nombre||`` sous le bloc ``||variables: définir Durée à ||``.

```blocks

let Durée = 0
input.onButtonPressed(Button.B, function () {
    let Chrono = 0
    Durée = input.runningTime() - Chrono
    basic.showNumber(0)
})

```

## Étape 10

Remplace la valeur ``||basic: 0||`` du bloc ``||basic: afficher nombre||`` par le bloc ``||math: ÷ entière||``.

```blocks

let Durée = 0
input.onButtonPressed(Button.B, function () {
    let Chrono = 0
    Durée = input.runningTime() - Chrono
    basic.showNumber(Math.idiv(0, 0))
})
```

## Étape 11

Remplace la valeur  ``||math: 0||`` de gauche par le bloc ``||variables: Durée||`` dans le bloc ``||math: ÷ entière||``.

Remplace la valeur  ``||math: 0||`` de droite par la valeur 1000 dans le bloc ``||math: ÷ entière||``.

```blocks

let Durée = 0
input.onButtonPressed(Button.B, function () {
    let Chrono = 0
    Durée = input.runningTime() - Chrono
    basic.showNumber(Math.idiv(Durée, 1000))
})

```

## Étape 12

Assure-toi que ta programmation est exacte.

Regarde l'indice!

```blocks

let Chrono = 0
let Durée = 0
input.onButtonPressed(Button.A, function () {
    Chrono = input.runningTime()
})
input.onButtonPressed(Button.B, function () {
    Durée = input.runningTime() - Chrono
    basic.showNumber(Math.idiv(Durée, 1000))
})

```

## Étape 13

Télécharge le programme dans le micro:bit.

Teste le programme!

Quelles sont les fonctions des boutons A et B ?