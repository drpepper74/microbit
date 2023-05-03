# Circuits électriques et servomoteur

# Tutoriel 1

## @showdialog

Programme le micro:bit pour qu'il active le servomoteur lorsqu'un bouton est pressé.

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

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Angle aigu||``.

Ajoute le bloc ``||variables: définir Angle aigu ||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

```blocks

let Angle_aigu = 0
input.onButtonPressed(Button.A, function () {
    Angle_aigu = 0
})


```

## Étape 5

Remplace la valeur ``|| variables : 0 ||`` du bloc ``|| variables : définir angle aigu ||`` par le bloc ``||math: choisir au hasard||``.

```blocks

let Angle_aigu = 0
input.onButtonPressed(Button.A, function () {
    Angle_aigu = randint(0, 10)
})

```

## Étape 6

Moidifie les valeurs ``||math: choisir au hasard||`` par les valeurs d'un angle aigu.

Remplace la valeur ``|| math : 0 ||`` par ``|| math : 1 ||``.

Remplace la valeur ``|| math : 10 ||`` par ``|| math : 89 ||``.

```blocks

let Angle_aigu = 0
input.onButtonPressed(Button.A, function () {
    Angle_aigu = randint(1, 89)
})


``

## Étape 7

Ajoute le bloc ``|| pins: régler position servo ||`` sous le bloc ``|| variables: définir angle aigu ||``

```blocks

let Angle_aigu = 0
input.onButtonPressed(Button.A, function () {
    Angle_aigu = randint(1, 89)
    pins.servoWritePin(AnalogPin.P0, 180)
})

```
## Étape 8

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P1 ||``.

Remplace la valeur ``|| pins: 180 ||`` par le bloc ``|| variables: angle aigu ||``.

```blocks

let Angle_aigu = 0
input.onButtonPressed(Button.A, function () {
    Angle_aigu = randint(1, 89)
    pins.servoWritePin(AnalogPin.P1, Angle_aigu)
})

```

## Étape 9

Ajoute le bloc ``|| basic: montrer nombre ||`` sous le bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| basic: 0 ||`` du bloc ``|| basic: montrer nombre ||`` par le bloc ``|| variables: angle aigu ||``.

```blocks

let Angle_aigu = 0
input.onButtonPressed(Button.A, function () {
    Angle_aigu = randint(1, 89)
    pins.servoWritePin(AnalogPin.P1, Angle_aigu)
    basic.showNumber(Angle_aigu)
})


```

## Étape 10

Ajoute le bloc ``|| basic: pause (ms) ||`` sous le bloc ``|| basic: montrer nombre ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||`` par la valeur ``|| basic: 5000 ||``.

```blocks

let Angle_aigu = 0
input.onButtonPressed(Button.A, function () {
    Angle_aigu = randint(1, 89)
    pins.servoWritePin(AnalogPin.P1, Angle_aigu)
    basic.showNumber(Angle_aigu)
    basic.pause(5000)
})

```

## Étape 11

Ajoute le bloc ``|| pins: régler position du servo ||`` sous le bloc ``|| basic: pause (ms) ||``.

Modifie le bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins : P1 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins : 0 ||``.

```blocks

let Angle_aigu = 0
input.onButtonPressed(Button.A, function () {
    Angle_aigu = randint(1, 89)
    pins.servoWritePin(AnalogPin.P1, Angle_aigu)
    basic.showNumber(Angle_aigu)
    basic.pause(5000)
    pins.servoWritePin(AnalogPin.P1, 0)
})


```

## Étape 4

Modifie les valeurs du bloc ``|| math: choisir au hasard ||``.

Remplace les valeurs ``|| math: 0 ||`` et ``|| math: 10 ||`` par les valeurs possibles d'un angle aigu.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P1, randint(0, 10))
})

## Étape 4

Ajoute le bloc 

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P1, randint(0, 10))
})


## Étape 4

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``||input: lorsque le bouton B est pressé||``.


```blocks

input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P0, 180)
})

```

## Étape 5

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P1 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 90 ||``.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P1, 90)
})


```

## Étape 6

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``||input: lorsque le bouton A+B est pressé||``.


```blocks

input.onButtonPressed(Button.AB, function () {
    pins.servoWritePin(AnalogPin.P0, 180)
})

```

## Étape 7

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P1 ||``.

La valeur ``|| pins: 180 ||`` demeure la même.

```blocks

input.onButtonPressed(Button.AB, function () {
    pins.servoWritePin(AnalogPin.P1, 180)
})


```

## Étape 8

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``||input: lorsque secouer||``.


```blocks

input.onGesture(Gesture.Shake, function () {
    pins.servoWritePin(AnalogPin.P0, 180)
})


```

## Étape 9

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P1 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 0 ||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    pins.servoWritePin(AnalogPin.P1, 0)
})

```

## @showdialog 

Félicitations! Tu as terminé de programmer un circuit électrique avec un servomoteur.

Pour tester le circuit, réalise les branchements et télécharge la programmation dans le micro:bit.