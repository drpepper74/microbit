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

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P1 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 0 ||``.

```blocks

pins.servoWritePin(AnalogPin.P1, 0)

```

## Étape 3

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Température||``.

Ajoute le bloc ``||variables: définir Température ||`` sous le bloc ``|| pins: régler position servo ||``.

```blocks

pins.servoWritePin(AnalogPin.P1, 0)
let Température = 0

```

## Étape 4

Remplace la valeur ``||variables: 0||`` du bloc ``||variables: définir Temperature ||`` par le bloc ``||input: température||``. 

```blocks

pins.servoWritePin(AnalogPin.P1, 0)
let Température = input.temperature()


```

## Étape 5

Ajoute le bloc ``|| basic: montrer nombre ||`` dans le bloc ``||basic: toujours||``.

```blocks

basic.forever(function () {
    basic.showNumber(0)
})

```

## Étape 6

Modifie le bloc ``|| basic: montrer nombre ||``.

Remplace la valeur ``|| basic: 0 ||`` du bloc ``|| basic: montrer nombre ||`` par le bloc ``||variables: Température ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
})

```

## Étape 7

Ajoute le bloc ``|| basic: pause (ms) ||`` sous le bloc ``|| basic: montrer nombre ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(100)
})

```

## Étape 8

Modifie le bloc ``|| basic: pause (ms) 100 ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||`` par la valeur ``|| basic: 1000 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
})

```

## Étape 9

Ajoute le bloc ``|| logic: si vrai alors ||`` sous le bloc ``|| basic: pause (ms) ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (true) {
    	
    }
})

```

## Étape 10

Modifie le bloc ``|| logic: si vrai alors ||``.

Remplace la valeur ``|| logic: vrai ||`` du bloc ``|| logic: si vrai alors ||`` par le bloc ``|| logic: 0 <= 0 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (0 <= 0) {
    	
    }
})

```

## Étape 11

Modifie le bloc ``|| logic: 0 <= 0 ||``.

Remplace la valeur ``|| logic: 0 ||`` de gauche par le bloc ``|| variables: Température ||``.

Remplace la valeur ``|| logic: 0 ||`` de droite par la valeur ``|| logic: 21 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
    	
    }
})

```

## Étape 12

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``|| logic: si vrai alors ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P0, 180)
    }
})

```

## Étape 13

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P1 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 45 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
    }
})

```

## Étape 14
Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| pins: régler position servo ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P0, 0)
    }
})

```

## Étape 15

Modifie les valeurs du bloc ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P12 ||``.

Remplace la valeur ``|| pins: 0 ||`` par ``|| pins: 1 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
    }
})

```

## Étape 16

Ajoute le bloc ``|| logic: si vrai alors ||`` sous le bloc ``|| logic: si vrai alors ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
    }
    if (true) {
    	
    }
})

```

## Étape 17

Modifie le bloc ``|| logic: si vrai alors ||``.

Remplace la valeur ``|| logic: vrai ||`` du bloc ``|| logic: si vrai alors ||`` par le bloc ``|| logic: et ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
    }
    if (false && false) {
    	
    }
})

```

## Étape 18

Modifie le bloc ``|| logic: et ||``.

Remplace la valeur ``|| logic: faux ||`` de gauche par le bloc ``|| logic: 0 >= 0 ||``.

Remplace la valeur ``|| logic: faux ||`` de droite par le bloc ``|| logic: 0 <= 0 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
    }
    if (0 >= 0 && 0 <= 0) {
    	
    }
})

```

## Étape 19

Modifie le bloc ``|| logic: 0 >= 0 ||``.

Remplace la valeur ``|| logic: 0 ||`` de gauche par le bloc ``|| variables: Température ||``.

Remplace la valeur ``|| logic: 0 ||`` de droite par la valeur ``|| logic: 22 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
    }
    if (Température >= 22 && 0 <= 0) {
    	
    }
})

```

## Étape 20

Modifie le bloc ``|| logic: 0 <= 0 ||``.

Remplace la valeur ``|| logic: 0 ||`` de gauche par le bloc ``|| variables: Température ||``.

Remplace la valeur ``|| logic: 0 ||`` de droite par la valeur ``|| logic: 27 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
    }
    if (Température >= 22 && Température <= 27) {
    	
    }
})

```

## Étape 21

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``|| logic: si vrai alors ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
    }
    if (Température >= 22 && Température <= 27) {
        pins.servoWritePin(AnalogPin.P0, 180)
    }
})

```

## Étape 22

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P1 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 90 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
    }
    if (Température >= 22 && Température <= 27) {
        pins.servoWritePin(AnalogPin.P1, 90)
    }
})

```

## Étape 23

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| pins: régler position servo ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
    }
    if (Température >= 22 && Température <= 27) {
        pins.servoWritePin(AnalogPin.P1, 90)
        pins.digitalWritePin(DigitalPin.P0, 0)
    }
})

```

## Étape 24

Modifie les valeurs du bloc ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P13 ||``.

Remplace la valeur ``|| pins: 0 ||`` par ``|| pins: 1 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
    }
    if (Température >= 22 && Température <= 27) {
        pins.servoWritePin(AnalogPin.P1, 90)
        pins.digitalWritePin(DigitalPin.P13, 1)
    }
})

```

## Étape 25

Ajoute le bloc ``|| logic: si vrai alors ||`` sous le bloc ``|| logic: si vrai alors ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
    }
    if (Température >= 22 && Température <= 27) {
        pins.servoWritePin(AnalogPin.P1, 90)
        pins.digitalWritePin(DigitalPin.P13, 1)
    }
    if (true) {
    	
    }
})


```

## Étape 26

Modifie le bloc ``|| logic: si vrai alors ||``.

Remplace la valeur ``|| logic: vrai ||`` du bloc ``|| logic: si vrai alors ||`` par le bloc ``|| logic: 0>=0 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
    }
    if (Température >= 22 && Température <= 27) {
        pins.servoWritePin(AnalogPin.P1, 90)
        pins.digitalWritePin(DigitalPin.P13, 1)
    }
    if (0 >= 0) {
    	
    }
})

```

## Étape 27

Modifie le bloc ``|| logic: 0 >= 0 ||``.

Remplace la valeur ``|| logic: 0 ||`` de gauche par le bloc ``|| variables: Température ||``.

Remplace la valeur ``|| logic: 0 ||`` de droite par la valeur ``|| logic: 28 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
    }
    if (Température >= 22 && Température <= 27) {
        pins.servoWritePin(AnalogPin.P1, 90)
        pins.digitalWritePin(DigitalPin.P13, 1)
    }
    if (Température >= 28) {
    	
    }
})


```

## Étape 28

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``|| logic: si vrai alors ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
    }
    if (Température >= 22 && Température <= 27) {
        pins.servoWritePin(AnalogPin.P1, 90)
        pins.digitalWritePin(DigitalPin.P13, 1)
    }
    if (Température >= 28) {
        pins.servoWritePin(AnalogPin.P0, 180)
    }
})

```

## Étape 29

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P1 ||``.

La valeur ``|| pins: 180 ||`` demeure la même.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
    }
    if (Température >= 22 && Température <= 27) {
        pins.servoWritePin(AnalogPin.P1, 90)
        pins.digitalWritePin(DigitalPin.P13, 1)
    }
    if (Température >= 28) {
        pins.servoWritePin(AnalogPin.P1, 180)
    }
})


```

## Étape 30

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| pins: régler position servo ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
    }
    if (Température >= 22 && Température <= 27) {
        pins.servoWritePin(AnalogPin.P1, 90)
        pins.digitalWritePin(DigitalPin.P13, 1)
    }
    if (Température >= 28) {
        pins.servoWritePin(AnalogPin.P1, 180)
        pins.digitalWritePin(DigitalPin.P0, 0)
    }
})


```

## Étape 31

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``|| logic: si et alors ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
    }
    if (Température >= 22 && Température <= 27) {
        pins.servoWritePin(AnalogPin.P1, 90)
        pins.digitalWritePin(DigitalPin.P13, 1)
    }
    if (Température >= 28) {
        pins.servoWritePin(AnalogPin.P1, 180)
        pins.digitalWritePin(DigitalPin.P0, 0)
    }
})

```

## Étape 32

Modifie les valeurs du bloc ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P14 ||``.

Remplace la valeur ``|| pins: 0 ||`` par ``|| pins: 1 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
    }
    if (Température >= 22 && Température <= 27) {
        pins.servoWritePin(AnalogPin.P1, 90)
        pins.digitalWritePin(DigitalPin.P13, 1)
    }
    if (Température >= 28) {
        pins.servoWritePin(AnalogPin.P1, 180)
        pins.digitalWritePin(DigitalPin.P14, 1)
    }
})

```

## Étape 33

Remplace le bloc ``||basic: toujours ||`` par le bloc ``||loops: chaque 500 (ms)||``.

Modifier la valeur ``||loops: 500||`` par ``||loops: 5000||``.

```blocks

loops.everyInterval(5000, function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
    }
    if (Température >= 22 && Température <= 27) {
        pins.servoWritePin(AnalogPin.P1, 90)
        pins.digitalWritePin(DigitalPin.P13, 1)
    }
    if (Température >= 28) {
        pins.servoWritePin(AnalogPin.P1, 180)
        pins.digitalWritePin(DigitalPin.P14, 1)
    }
})

```

## @showdialog 

Félicitations! Tu as terminé de programmer un circuit électrique avec un servomoteur.

Pour tester le circuit, réalise les branchements et télécharge la programmation dans le micro:bit.
