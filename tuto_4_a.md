# Niveau 4

# Tutoriel Bonus A

## @showdialog

Affiche la température ambiante sur le micro:bit à l'aide d'un graphique.

## Étape 1

Supprime le bloc ``||basic:toujours||``

## Étape 2

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Temperature||``.

Ajoute le bloc ``||variables: définir Temperature à 0||`` dans le bloc ``||basic: Au démarrage||``.

```blocks

let Temperature = 0

```

## Étape 3

Remplace la valeur ``||variables: 0||`` du bloc ``||variables: définir Temperature||`` par le bloc ``||input: température||``. 

```blocks

let Temperature = input.temperature()

```

## Étape 4

Ajoute le bloc ``||led: tracer le graphique||`` dans le bloc ``||input: lorsque le bouton A+B est pressé||``.

```blocks

input.onButtonPressed(Button.AB, function () {
    led.plotBarGraph(
    0,
    0
    )
})
let Temperature = input.temperature()

```

## Étape 5

Remplace la première valeur ``|| led: 0||`` du bloc ``|| led: tracer le graphique||`` par le bloc ``||variables: Temperature||``.

```blocks

input.onButtonPressed(Button.AB, function () {
    led.plotBarGraph(
    Temperature,
    0
    )
})
let Temperature = 0
Temperature = input.temperature()

```

## Étape 6

Remplace la deuxième valeur ``|| led: 0||`` du bloc ``|| led: tracer le graphique||`` par la valeur ``|| led: 50||``.

```blocks

input.onButtonPressed(Button.AB, function () {
    led.plotBarGraph(
    Temperature,
    50
    )
})
let Temperature = 0
Temperature = input.temperature()

```

## Étape 7

Télécharge le programme dans le micro:bit.

Teste le programme!

Manipule le micro:bit. Que remarques-tu?