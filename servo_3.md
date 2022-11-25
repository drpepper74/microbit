# Circuits électriques et servomoteur

# Tutoriel 1

## @showdialog

Programme le micro:bit pour qu'il active le servomoteur à un angle précis en fonction de l'intensité lumineuse.

## Étape 1

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``||basic: au démarrage||``.

```blocks

pins.servoWritePin(AnalogPin.P0, 180)

```

## Étape 2

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P3 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 0 ||``.

```blocks

pins.servoWritePin(AnalogPin.P3, 0)

```

## Étape 3

Ajoute le bloc ``|| basic: montrer nombre ||`` dans le bloc ``||basic: toujours||``.

```blocks

basic.forever(function () {
    basic.showNumber(0)
})

```

## Étape 4

Modifie le bloc ``|| basic: montrer nombre ||``.

Remplace la valeur ``|| basic: 0 ||`` du bloc ``|| basic: montrer nombre ||`` par le bloc ``|| input: niveau d'intensité lumineuse ||``.

```blocks

basic.forever(function () {
    basic.showNumber(input.lightLevel())
})

```

## Étape 5

Ajoute le bloc ``|| basic: pause (ms) ||`` sous le bloc ``|| basic: montrer nombre ||``.

```blocks

basic.forever(function () {
    basic.showNumber(input.lightLevel())
    basic.pause(100)
})

```

## Étape 6

Modifie le bloc ``|| basic: pause (ms) 100 ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||`` par la valeur ``|| basic: 1000 ||``.

```blocks

basic.forever(function () {
    basic.showNumber(input.lightLevel())
    basic.pause(1000)
})

```

## Étape 7

Ajoute le bloc ``|| logic: si vrai alors ||`` sous le bloc ``|| basic: pause (ms) ||``.

```blocks

basic.forever(function () {
    basic.showNumber(input.lightLevel())
    basic.pause(1000)
    if (true) {
    	
    }
})

```

## Étape 8

Modifie le bloc ``|| logic: si vrai alors ||``.

Remplace la valeur ``|| logic: vrai ||`` du bloc ``|| logic: si vrai alors ||`` par le bloc ``|| logic: 0 <= 0 ||``.

```blocks

basic.forever(function () {
    basic.showNumber(input.lightLevel())
    basic.pause(1000)
    if (0 <= 0) {
    	
    }
})

```

## Étape 9

Modifie le bloc ``|| logic: 0 <= 0 ||``.

Remplace la valeur ``|| logic: 0 ||`` de gauche par le bloc ``|| input: niveau d'intensité lumineuse ||``.

Remplace la valeur ``|| logic: 0 ||`` de droite par la valeur ``|| logic: 40 ||``.

```blocks

basic.forever(function () {
    basic.showNumber(input.lightLevel())
    basic.pause(1000)
    if (input.lightLevel() <= 40) {
    	
    }
})

```

## Étape 10

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``|| logic: si vrai alors ||``.

```blocks

basic.forever(function () {
    basic.showNumber(input.lightLevel())
    basic.pause(1000)
    if (input.lightLevel() <= 40) {
        pins.servoWritePin(AnalogPin.P0, 180)
    }
})

```

## Étape 11

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P3 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 100 ||``.

```blocks

basic.forever(function () {
    basic.showNumber(input.lightLevel())
    basic.pause(1000)
    if (input.lightLevel() <= 40) {
        pins.servoWritePin(AnalogPin.P3, 100)
    }
})

```

## Étape 12
Ajoute le bloc ``|| logic: si vrai alors ||`` sous le bloc ``|| logic: si vrai alors ||``.

```blocks

basic.forever(function () {
    basic.showNumber(input.lightLevel())
    basic.pause(1000)
    if (input.lightLevel() <= 40) {
        pins.servoWritePin(AnalogPin.P3, 100)
    }
    if (true) {
    	
    }
})

```

## Étape 13

Modifie le bloc ``|| logic: si vrai alors ||``.

Remplace la valeur ``|| logic: vrai ||`` du bloc ``|| logic: si vrai alors ||`` par le bloc ``|| logic: 0 >= 0 ||``.

```blocks

basic.forever(function () {
    basic.showNumber(input.lightLevel())
    basic.pause(1000)
    if (input.lightLevel() <= 40) {
        pins.servoWritePin(AnalogPin.P3, 100)
    }
    if (0 >= 0) {
    	
    }
})

```

## Étape 14

Modifie le bloc ``|| logic: 0 >= 0 ||``.

Remplace la valeur ``|| logic: 0 ||`` de gauche par le bloc ``|| input: niveau d'intensité lumineuse ||``.

Remplace la valeur ``|| logic: 0 ||`` de droite par la valeur ``|| logic: 41 ||``.

```blocks

basic.forever(function () {
    basic.showNumber(input.lightLevel())
    basic.pause(1000)
    if (input.lightLevel() <= 40) {
        pins.servoWritePin(AnalogPin.P3, 100)
    }
    if (input.lightLevel() >= 41) {
    	
    }
})

```

## Étape 15

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``|| logic: si vrai alors ||``.

```blocks

basic.forever(function () {
    basic.showNumber(input.lightLevel())
    basic.pause(1000)
    if (input.lightLevel() <= 40) {
        pins.servoWritePin(AnalogPin.P3, 100)
    }
    if (input.lightLevel() >= 41) {
        pins.servoWritePin(AnalogPin.P0, 180)
    }
})


```

## Étape 16

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P3 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 50 ||``.

```blocks

basic.forever(function () {
    basic.showNumber(input.lightLevel())
    basic.pause(1000)
    if (input.lightLevel() <= 40) {
        pins.servoWritePin(AnalogPin.P3, 100)
    }
    if (input.lightLevel() >= 41) {
        pins.servoWritePin(AnalogPin.P3, 50)
    }
})

```

## @showdialog 

Félicitations! Tu as terminé de programmer un circuit électrique avec un servomoteur.

Pour tester le circuit, réalise les branchements et télécharge la programmation dans le micro:bit.
