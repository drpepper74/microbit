# Circuits électriques et servomoteur

# Tutoriel 6

## @showdialog

Transforme le circuit électrique afin de créer une barrière et des feux de circulation. 


## Étape 1

Conserve les blocs ``||basic:au démarrage||`` et ``||basic:toujours||``.

```blocks

basic.forever(function () {
	
})

```

## Étape 2

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``||basic: au démarrage||``.

```blocks

pins.servoWritePin(AnalogPin.P0, 180)

```

## Étape 3

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P2 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 0 ||``.

```blocks

pins.servoWritePin(AnalogPin.P2, 0)

```

## Étape 4

Ajoute trois blocs ``|| pins: écrire sur la broche ||`` sous le bloc ``|| pins: régler position servo ||``.

P12 = Vert - P13 = Jaune - P14 = Rouge

```blocks

pins.servoWritePin(AnalogPin.P2, 0)
pins.digitalWritePin(DigitalPin.P0, 0)
pins.digitalWritePin(DigitalPin.P0, 0)
pins.digitalWritePin(DigitalPin.P0, 0)

```

## Étape 5

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace les valeurs ``|| pins: P0 ||`` par ``|| pins: P12 ||``, ``|| pins: P13 ||`` et ``|| pins: P14 ||``.

Remplace les valeurs ``|| pins: 0 ||`` par ``|| pins: 0 ||``, ``|| pins: 0 ||`` et ``|| pins: 1 ||``.

P12 = Vert - P13 = Jaune - P14 = Rouge

```blocks

pins.servoWritePin(AnalogPin.P2, 0)
pins.digitalWritePin(DigitalPin.P12, 0)
pins.digitalWritePin(DigitalPin.P13, 0)
pins.digitalWritePin(DigitalPin.P14, 1)

```

## Étape 6

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P0, 180)
})

```

## Étape 7

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P2 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 90 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
})

```

## Étape 8

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| pins: régler position servo ||``.

P12 = Vert - P13 = Jaune - P14 = Rouge

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P0, 0)
    })

```

## Étape 9

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P14 ||``.

Remplace la valeur ``|| pins: 0 ||`` par ``|| pins: 1 ||``.

Regarde l'indice!

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
})

```

## Étape 10

Ajoute le bloc ``|| basic: pause (ms) ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||`` par la valeur ``|| basic: 1000 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
})

```

## Étape 11

Ajoute le bloc ``|| basic: montrer l'icône  ||`` sous le bloc ``|| basic: pause (ms) ||``.

Regarde l'indice.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
})

```

## Étape 12

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| basic: montrer l'icône ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 13

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P14 ||``.

La valeur ``|| pins: 0 ||`` demeure la même.


```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
})


```

## Étape 14

Ajoute le bloc ``|| basic: pause (ms) ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

La valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||`` demeure la même.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
})


```

## Étape 15

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| basic: pause (ms) ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 16

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P13 ||``.

Remplace la valeur ``|| pins: 0 ||`` par ``|| pins: 1 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
})

```

## Étape 17

Ajoute le bloc ``|| basic: pause (ms) ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||`` par la valeur ``|| basic: 1000 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(1000)
})

```

## Étape 18

Ajoute le bloc ``|| basic: montrer LEDs ||`` sous le bloc ``|| basic: pause (ms) ||``.

Dessine un petit X.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(1000)
    basic.showLeds(`
        . . . . .
        . # . # .
        . . # . .
        . # . # .
        . . . . .
        `)
})

```

## Étape 19

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| basic: montrer LEDs ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(1000)
    basic.showLeds(`
        . . . . .
        . # . # .
        . . # . .
        . # . # .
        . . . . .
        `)
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 20

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P13 ||``.

Remplace la valeur ``|| pins: 0 ||`` par ``|| pins: 0 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(1000)
    basic.showLeds(`
        . . . . .
        . # . # .
        . . # . .
        . # . # .
        . . . . .
        `)
    pins.digitalWritePin(DigitalPin.P13, 0)
})

```

## Étape 21

Ajoute le bloc ``|| basic: pause (ms) ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

La valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||`` demeure la même.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(1000)
    basic.showLeds(`
        . . . . .
        . # . # .
        . . # . .
        . # . # .
        . . . . .
        `)
    pins.digitalWritePin(DigitalPin.P13, 0)
    basic.pause(100)
})

```

## Étape 22

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| basic: pause (ms) ||``.


```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(1000)
    basic.showLeds(`
        . . . . .
        . # . # .
        . . # . .
        . # . # .
        . . . . .
        `)
    pins.digitalWritePin(DigitalPin.P13, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P0, 0)
})


```

## Étape 23

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P12 ||``.

Remplace la valeur ``|| pins: 0 ||`` par ``|| pins: 1 ||``.

Regarde l'indice!

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(1000)
    basic.showLeds(`
        . . . . .
        . # . # .
        . . # . .
        . # . # .
        . . . . .
        `)
    pins.digitalWritePin(DigitalPin.P13, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P12, 1)
})


```

## Étape 24

Ajoute le bloc ``|| basic: pause (ms) ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||`` par la valeur ``|| basic: 1000 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(1000)
    basic.showLeds(`
        . . . . .
        . # . # .
        . . # . .
        . # . # .
        . . . . .
        `)
    pins.digitalWritePin(DigitalPin.P13, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P12, 1)
    basic.pause(1000)
})


```

## Étape 25

Ajoute le bloc ``|| basic: montrer l'icône  ||`` sous le bloc ``|| basic: pause (ms) ||``.

Regarde l'indice.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(1000)
    basic.showLeds(`
        . . . . .
        . # . # .
        . . # . .
        . # . # .
        . . . . .
        `)
    pins.digitalWritePin(DigitalPin.P13, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P12, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.Yes)
})


```

## @showdialog 

Félicitations! Tu as terminé de programmer une barrière.

Pour tester le circuit, réalise les branchements et télécharge la programmation dans le micro:bit.