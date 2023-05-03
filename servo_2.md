# Circuits électriques et servomoteur

# Tutoriel 2

## @showdialog

Programme le micro:bit pour qu'il active le servomoteur à un angle aléatoire et à un angle précis lorsqu'un bouton est pressé.

De plus, le micro:bit doit affiché l'angle réalisé par le servomoteur.

## Étape 1

Supprime le bloc ``||basic:toujours||``.

## Étape 2

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``||basic:au démarrage||``.

```blocks

pins.servoWritePin(AnalogPin.P0, 180)

```

## Étape 3

Modifie le bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins : P1 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins : 0 ||``.

```blocks

pins.servoWritePin(AnalogPin.P1, 0)

```

## Étape 4

Crée une ``||variables: variable||`` et donne lui le nom ``||variables: Angle||``.

Ajoute le bloc ``||variables: définir Angle||`` dans le bloc ``||input: lorsque le bouton A est appuyé||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = 0
})

```

## Étape 5

Remplace la valeur ``||variables: 0||`` du bloc ``||variables: définir Angle ||`` par le bloc ``||math: choisir au hasard de 0 à 10||``. 

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(0, 10)
})

```

## Étape 6

Remplace la valeur ``||math: 0||`` du bloc ``||math: choisir au hasard de 0 à 10 ||`` par la valeur ``||math: 1||``.

Remplace la valeur ``||math: 10||`` du bloc ``||math: choisir au hasard de 0 à 10 ||`` par la valeur ``||math: 180||``. 

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 180)
})

```

## Étape 7

Ajoute le bloc ``|| pins: régler position servo ||`` sous le bloc ``||variables: définir Angle ||``.


```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 180)
    pins.servoWritePin(AnalogPin.P0, 180)
})

```

## Étape 8

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P2 ||``.

Remplace la valeur ``|| pins: 180 ||`` par le bloc ``||variables:  Angle ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 180)
    pins.servoWritePin(AnalogPin.P2, Angle)
})

```

## Étape 9

Ajoute le bloc ``|| basic: montre nombre ||`` sous le bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| basic: 0 ||`` du bloc ``|| basic: montrer nombre ||`` par le bloc ``|| variables: Angle ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 180)
    pins.servoWritePin(AnalogPin.P2, Angle)
    basic.showNumber(Angle)
})

```

## Étape 10

Ajoute le bloc ``|| basic: pause (ms) 100 ||`` sous le bloc ``|| basic: montrer nombre ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||`` par la valeur ``|| basic: 2000 ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 180)
    pins.servoWritePin(AnalogPin.P2, Angle)
    basic.showNumber(Angle)
    basic.pause(2000)
})


```

## Étape 11

Ajoute le bloc ``|| pins: régler position servo ||`` sous le bloc ``||basic: pause (ms) 2000 ||``.


```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 180)
    pins.servoWritePin(AnalogPin.P2, Angle)
    basic.showNumber(Angle)
    basic.pause(2000)
    pins.servoWritePin(AnalogPin.P0, 180)
})

```

## Étape 12

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| pins: P0 ||`` par la valeur ``|| pins: P2 ||``.

Remplace la valeur ``|| pins: 180 ||`` par la valeur ``|| pins: 0 ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 180)
    pins.servoWritePin(AnalogPin.P2, Angle)
    basic.showNumber(Angle)
    basic.pause(2000)
    pins.servoWritePin(AnalogPin.P2, 0)
})

```

## @showdialog 

Félicitations! Tu as terminé de programmer un circuit électrique avec un servomoteur.

Pour tester le circuit, réalise les branchements et télécharge la programmation dans le micro:bit.