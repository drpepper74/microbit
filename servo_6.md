# Circuits électriques et servomoteur

# Tutoriel 1

## @showdialog

Programme le micro:bit pour qu'il active le servomoteur à un angle précis en fonction de la température.

De plus, le micro:bit doit actvité une lumière.

## Étape 1

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``||basic: au démarrage||``.

```blocks

pins.servoWritePin(AnalogPin.P0, 180)

```

## Étape 2

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P2 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 0 ||``.

```blocks

pins.servoWritePin(AnalogPin.P2, 0)

```

## Étape 3

Ajoute trois blocs ``|| pins: écrire sur la broche ||`` sous le bloc ``|| pins: régler position servo ||``.

P12 = Vert - P12 = Jaune - P14 = Rouge

```blocks

pins.servoWritePin(AnalogPin.P2, 0)
pins.digitalWritePin(DigitalPin.P0, 0)
pins.digitalWritePin(DigitalPin.P0, 0)
pins.digitalWritePin(DigitalPin.P0, 0)

```

## Étape 4

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace les valeurs ``|| pins: P0 ||`` par ``|| pins: P12 ||``, ``|| pins: P13 ||`` et ``|| pins: P14 ||``.

Remplace les valeurs ``|| pins: 0 ||`` par ``|| pins: 0 ||``, ``|| pins: 0 ||`` et ``|| pins: 1 ||``.


```blocks

pins.servoWritePin(AnalogPin.P2, 0)
pins.digitalWritePin(DigitalPin.P12, 0)
pins.digitalWritePin(DigitalPin.P13, 0)
pins.digitalWritePin(DigitalPin.P14, 1)

```

## Étape 5

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P0, 180)
})

```

## Étape 6

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P2 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 90 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
})

```

## Étape 7

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| pins: régler position servo ||``.

P12 = Vert - P12 = Jaune - P14 = Rouge

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P0, 0)
    })

```

## Étape 8

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

## Étape 9

Ajoute le bloc ``|| basic: pause (ms) ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||`` par la valeur ``|| basic: 500 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(500)
})

```

## Étape 10

Ajoute le bloc ``|| basic: montrer l'icône  ||`` sous le bloc ``|| basic: pause (ms) ||``.

Regarde l'indice.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(500)
    basic.showIcon(IconNames.No)
})

```

## Étape 11

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| basic: montrer l'icône ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(500)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 12

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P14 ||``.

La valeur ``|| pins: 0 ||`` demeure la même.


```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(500)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
})


```

## Étape 13

Ajoute le bloc ``|| basic: pause (ms) ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

La valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||`` demeure la même.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(500)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
})


```

## Étape 14

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| pins: régler position servo ||``.

P12 = Vert - P12 = Jaune - P14 = Rouge

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P0, 0)
    })

```

## Étape 15

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

## Étape 16

Ajoute le bloc ``|| basic: pause (ms) ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||`` par la valeur ``|| basic: 500 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(500)
})

```

## Étape 17

Ajoute le bloc ``|| basic: montrer l'icône  ||`` sous le bloc ``|| basic: pause (ms) ||``.

Regarde l'indice.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(500)
    basic.showIcon(IconNames.No)
})

```

## Étape 18

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| basic: montrer l'icône ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(500)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 19

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P14 ||``.

La valeur ``|| pins: 0 ||`` demeure la même.


```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(500)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
})


```

## Étape 20

Ajoute le bloc ``|| basic: pause (ms) ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

La valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||`` demeure la même.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(500)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
})

```

## Étape 21

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| basic: pause (ms) ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(500)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 22

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P13 ||``.

Remplace la valeur ``|| pins: 0 ||`` par ``|| pins: 1 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(500)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
})

```

## Étape 23

Ajoute le bloc ``|| basic: pause (ms) ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||`` par la valeur ``|| basic: 500 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(500)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(500)
})

```

## Étape 24

Ajoute le bloc ``|| basic: montrer LEDs ||`` sous le bloc ``|| basic: pause (ms) ||``.

Dessine un petit X.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(500)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(500)
    basic.showLeds(`
        . . . . .
        . # . # .
        . . # . .
        . # . # .
        . . . . .
        `)
})

```

## Étape 25

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| basic: montrer LEDs ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(500)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(500)
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

## Étape 26

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P13 ||``.

Remplace la valeur ``|| pins: 0 ||`` par ``|| pins: 0 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(500)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(500)
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

## Étape 27

Ajoute le bloc ``|| basic: pause (ms) ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

La valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||`` demeure la même.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(500)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(500)
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

## Étape 28

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| basic: pause (ms) ||``.


```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(500)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(500)
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

## Étape 29

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P12 ||``.

Remplace la valeur ``|| pins: 0 ||`` par ``|| pins: 1 ||``.

Regarde l'indice!

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(500)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(500)
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

## Étape 30

Ajoute le bloc ``|| basic: pause (ms) ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||`` par la valeur ``|| basic: 500 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(500)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(500)
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
    basic.pause(500)
})


```

## Étape 31

Ajoute le bloc ``|| basic: montrer l'icône  ||`` sous le bloc ``|| basic: pause (ms) ||``.

Regarde l'indice.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(500)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(500)
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
    basic.pause(500)
    basic.showIcon(IconNames.Yes)
})


```

## Étape 32

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| basic: montrer l'icône ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(500)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(500)
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
    basic.pause(500)
    basic.showIcon(IconNames.Yes)
    pins.digitalWritePin(DigitalPin.P0, 0)
})


```

## Étape 33

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P12 ||``.

La valeur ``|| pins: 0 ||`` demeure la même.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(500)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(500)
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
    basic.pause(500)
    basic.showIcon(IconNames.Yes)
    pins.digitalWritePin(DigitalPin.P12, 0)
})

```