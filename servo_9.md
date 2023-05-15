# Circuits électriques et servomoteur

# Tutoriel 8

## @showdialog

Programme le micro:bit pour qu'il active le servomoteur à un angle précis en fonction.

De plus, le micro:bit doit activer une lumière en fonction du degré réalisé.


## Étape 1

Supprime le bloc ``||basic:toujours||``.


## Étape 2

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Angle||``.

Ajoute le bloc ``||variables: définir Angle ||`` dans le bloc ``||basic:au démarrage||``.

```blocks

let Angle = 0

```

## Étape 3

Ajoute le bloc ``||pins: régler position servo ||`` sous le bloc ``||variables:définir Angle||``.

Remplace la valeur ``||pins: P0 ||`` par ``||pins: P2 ||``.

Remplace la valeur ``||pins: 180 ||`` par ``||pins: 0 ||``.

```blocks

let Angle = 0
pins.servoWritePin(AnalogPin.P2, 0)

```

## Étape 4

Ajoute les blocs ``||pins: écrire sur la broche ||`` sous le bloc ``||pins:régler position servo||``.

Remplace les valeurs ``||pins: P0 ||`` par ``||pins: P12 ||``, ``||pins: P13 ||` et ``||pins: P14 ||`.

Les valeurs ``||pins: 0 ||`` demeurent les mêmes.

```blocks

let Angle = 0
pins.servoWritePin(AnalogPin.P2, 0)
pins.digitalWritePin(DigitalPin.P0, 0)
pins.digitalWritePin(DigitalPin.P0, 0)
pins.digitalWritePin(DigitalPin.P0, 0)

```

## Étape 5

Ajoute le bloc ``||loops: répéter ||`` dans le bloc ``||input:lorsque le bouton A est pressé||``.

Remplace la valeur ``||loops: 4 ||`` par ``||loops: 36 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 36; index++) {
    	
    }
})

```

## Étape 6

Ajoute le bloc ``||variables: modifier Angle ||`` dans le bloc ``||loops:répéter||``.

Remplace la valeur ``||variables: 1 ||`` par ``||variables: 5 ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 36; index++) {
        Angle += 5
    }
})

```

## Étape 7

Ajoute le bloc ``||pins: régler position servo ||`` sous le bloc ``||variables:modifier Angle||``.

Remplace la valeur ``||pins: P0 ||`` par la valeur ``||pins: P2 ||``.

Remplace la valeur ``||pins: 180 ||`` par le bloc ``||variables: Angle ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 36; index++) {
        Angle += 5
        pins.servoWritePin(AnalogPin.P2, Angle)
    }
})

```

## Étape 8

Ajoute le bloc ``||basic: pause (ms) ||`` sous le bloc ``||pins:régler position servo||``.

Remplace la valeur ``||basic: 100 ||`` par la valeur ``||basic: 500 ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 36; index++) {
        Angle += 5
        pins.servoWritePin(AnalogPin.P2, Angle)
        basic.pause(500)
    }
})

```

## Étape 9

Ajoute le bloc ``||logic: si vrai alors ||`` sous le bloc ``||basic:pause (ms)||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 36; index++) {
        Angle += 5
        pins.servoWritePin(AnalogPin.P2, Angle)
        basic.pause(500)
    }
})

```