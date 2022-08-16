# Niveau 4

# Tutoriel Bonus B

## @showdialog

Affiche la luminosité ambiante de la pièce sur le micro:bit à l'aide d'un graphique.

## Étape 1

Supprime le bloc ``||basic:toujours||``

## Étape 2

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:LED||``.

Ajoute le bloc ``||variables: définir LED à 0||`` dans le bloc ``||basic: Au démarrage||``.

```blocks

let LED = 0

```

## Étape 3

Remplace la valeur ``||variables: 0||`` du bloc ``||variables: définir LED||`` par le bloc ``||input: niveau d'intensité lumineuse||``. 

```blocks

let LED = input.lightLevel()

```

## Étape 4

Ajoute le bloc ``||led: tracer le graphique||`` dans le bloc ``||input: lorsque le bouton A+B est pressé||``.

```blocks

input.onButtonPressed(Button.AB, function () {
    led.plotBarGraph(
    0,
    255
    )
})
let LED = input.lightLevel()


```

## Étape 5

Remplace la première valeur ``|| led: 0||`` du bloc ``|| led: tracer le graphique||`` par le bloc ``||variables: LED||``.

```blocks

input.onButtonPressed(Button.AB, function () {
    led.plotBarGraph(
    LED,
    255
    )
})
let LED = 0
LED = input.lightLevel()

```

## Étape 6

Remplace la deuxième valeur ``|| led: 0||`` du bloc ``|| led: tracer le graphique||`` par la valeur ``|| led: 255||``.

```blocks

input.onButtonPressed(Button.AB, function () {
    led.plotBarGraph(
    LED,
    255
    )
})
let LED = 0
LED = input.lightLevel()


```

## Étape 7

Télécharge le programme dans le micro:bit.

Teste le programme!

Manipule le micro:bit. Que remarques-tu?