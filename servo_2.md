# Circuits électriques et servomoteur

# Tutoriel 2

## @showdialog

Programme le micro:bit pour qu'il active le servomoteur à un angle aléatoire lorsqu'un bouton est pressé.

De plus, affiche l'angle réalisé par le servomoteur.

## Étape 1

Conserve les blocs ``||basic:au démarrage||`` et ``||basic:toujours||``.

```blocks

basic.forever(function () {
	
})

```

## Étape 2

Crée une ``||variables: variable||`` et donne lui le nom ``||variables: Angle||``.

Ajoute le bloc ``||variables: définir Angle||`` dans le bloc ``||input: lorsque le bouton A est appuyé||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = 0
})

```

## Étape 3

Remplace la valeur ``||variables: 0||`` du bloc ``||variables: définir Angle ||`` par le bloc ``||math: choisir au hasard de 0 à 10||``. 

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(0, 10)
})

```

## Étape 4

Remplace la valeur ``||math: 0||`` du bloc ``||math: choisir au hasard de 0 à 10 ||`` par la valeur ``||math: 1||``.

Remplace la valeur ``||math: 10||`` du bloc ``||math: choisir au hasard de 0 à 10 ||`` par la valeur ``||math: 180||``. 

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 180)
})

```

## Étape 5

Ajoute le bloc ``|| pins: régler position servo ||`` sous le bloc ``||variables: définir Angle ||``.


```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 180)
    pins.servoWritePin(AnalogPin.P0, 180)
})

```

## Étape 6

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

## Étape 7

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

## Étape 8

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

## Étape 9

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

## Étape 10

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