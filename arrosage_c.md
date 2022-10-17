# Système d'arrosage automatisé

## @showdialog
Programme les différentes composants du système d'arrosage automatisé.

## Étape 1

Ajoute le bloc ``|| pins: écrire sur la broche ||`` dans le bloc ``||basic: au démarrage||``.

```blocks

pins.digitalWritePin(DigitalPin.P0, 0)

```
## Étape 2

Modifie la valeur ``|| pins: P0 ||`` du bloc ``|| pins: écrire sur la broche ||`` par ``|| pins: P2 ||``.

La valeur  ``|| pins: 0 ||`` du bloc ``|| pins: écrire sur la broche ||`` demeure la même.

```blocks

pins.digitalWritePin(DigitalPin.P2, 0)

```

## Étape 3

Ajoute le bloc ``|| input: lorsque le bouton A est pressé. ||`` dans la zone de programmation.

Ajoute le bloc ``|| basic: montrer nombre ||`` dans le bloc ``|| input: lorsque le bouton A est pressé. ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    basic.showNumber(0)
})

```

## Étape 4

Remplace la valeur ``|| basic: 0 ||`` du bloc ``|| basic: montrer nombre ||`` par le bloc ``|| math: arrondi ||``

```blocks

input.onButtonPressed(Button.A, function () {
    basic.showNumber(Math.round(0))
})

```

## Étape 5

Remplace la valeur ``|| math: 0 ||`` du bloc ``|| math: arrondi ||`` par le bloc ``|| pins: lire la broche analogique ||``

```blocks

input.onButtonPressed(Button.A, function () {
    basic.showNumber(Math.round(pins.analogReadPin(AnalogPin.P0)))
})

```

## Étape 6

Modifie la valeur ``|| pins: P0 ||`` du bloc ``|| pins: lire la broche analogique ||`` par ``|| pins: P1 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    basic.showNumber(Math.round(pins.analogReadPin(AnalogPin.P1)))
})

```

## Étape 7

Ajoute le bloc ``|| input: lorsque le bouton B est pressé. ||``.

Ajoute le bloc ``|| pins: écrire sur la broche ||`` dans le bloc ``|| input: lorsque le bouton B est pressé. ||``.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 8

Modifie la valeur ``|| pins: P0 ||`` du bloc ``|| pins: écrire sur la broche ||`` par ``|| pins: P2 ||``.

Modifie la valeur ``|| pins: 0 ||`` du bloc ``|| pins: écrire sur la broche ||`` par ``|| pins: 1 ||``.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.digitalWritePin(DigitalPin.P2, 1)
})

```

## Étape 9

Ajoute le bloc ``|| basic: pause (ms) ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Modifie la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||`` par ``|| basic: 30000 ||``.

Si ``|| basic: 1 seconde ||`` = ``|| basic: 1 000 ms ||`` donc ``|| basic: 30 secondes ||`` = ``|| basic: 30 000 ms ||``

```blocks

input.onButtonPressed(Button.B, function () {
    pins.digitalWritePin(DigitalPin.P2, 1)
    basic.pause(30000)
})

```

## Étape 10

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| basic: pause (ms) 30000. ||``.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.digitalWritePin(DigitalPin.P2, 1)
    basic.pause(1000)
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 11

Modifie la valeur ``|| pins: P0 ||`` du bloc ``|| pins: écrire sur la broche ||`` par ``|| pins: P2 ||``.

La valeur ``|| pins: 0 ||`` du bloc ``|| pins: écrire sur la broche ||`` demeure la même.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.digitalWritePin(DigitalPin.P2, 1)
    basic.pause(1000)
    pins.digitalWritePin(DigitalPin.P2, 0)
})

```


## Étape 12

Ajoute le bloc ``|| logic: si vrai alors sinon ||`` dans le bloc ``|| basic: toujours ||``.

```blocks

basic.forever(function () {
    if (true) {
    	
    } else {
    	
    }
})

```

## Étape 13

Remplace la valeur ``|| logic: vrai ||`` du bloc ``|| logic: si vrai alors ||`` par le bloc ``|| logic: 0 < 0 ||``.

Modifie la valeur ``||logic: < ||`` du bloc ``|| logic: 0 < 0 ||`` par la valeur ``||logic: > ||``.

```blocks

basic.forever(function () {
    if (0 > 0) {
    	
    } else {
    	
    }
})


```

## Étape 14

Remplace la valeur ``|| logic: 0 ||`` de gauche du bloc ``|| logic: 0 < 0 ||`` par le bloc ``|| math: arrondi ||``.

```blocks

basic.forever(function () {
    if (Math.round(0) > 0) {
    	
    } else {
    	
    }
})


```

## Étape 15

Remplace la valeur ``|| math: 0 ||``  du bloc ``|| math: arrondi ||`` par le bloc ``|| pins: lire la broche analogique ||``.

```blocks

basic.forever(function () {
    if (Math.round(pins.analogReadPin(AnalogPin.P0)) > 0) {
    	
    } else {
    	
    }
})

```

## Étape 16

Modifie la valeur ``|| pins: P0 ||``  du bloc ``|| pins: lire la broche ||`` par ``|| pins: P1 ||``.

```blocks

basic.forever(function () {
    if (Math.round(pins.analogReadPin(AnalogPin.P1)) > 0) {
    	
    } else {
    	
    }
})

```

## Étape 17

Modifie la valeur ``|| logic: 0 ||`` de droite du bloc ``|| logic: si vrai alors ||`` par ``|| logic: 550 ||``.

```blocks

basic.forever(function () {
    if (Math.round(pins.analogReadPin(AnalogPin.P0)) > 550) {
    	
    } else {
    	
    }
})

```

## Étape 18

Ajoute le bloc ``|| basic: montrer nombre ||`` dans le bloc ``|| logic: si alors ||``.

```blocks

basic.forever(function () {
    if (Math.round(pins.analogReadPin(AnalogPin.P0)) > 0) {
        basic.showNumber(0)
    } else {
    	
    }
})

```

## Étape 19

Remplace la valeur ``|| basic: 0 ||`` du bloc ``|| basic: montrer nombre ||`` par le bloc ``|| pins: lire la broche analogique ||``.

```blocks

basic.forever(function () {
    if (Math.round(pins.analogReadPin(AnalogPin.P0)) > 0) {
        basic.showNumber(pins.analogReadPin(AnalogPin.P))
    } else {
    	
    }
})


```

## Étape 20

Modifie la valeur ``|| pins: P0 ||`` du bloc ``|| pins: lire la broche analogique ||`` par ``|| pins: P1 ||``.

```blocks

basic.forever(function () {
    if (Math.round(pins.analogReadPin(AnalogPin.P0)) > 0) {
        basic.showNumber(pins.analogReadPin(AnalogPin.P1))
    } else {
    	
    }
})

```

## Étape 21

Ajoute le bloc ``|| basic: montrer l'icône ||`` sous le bloc ``|| basic: montrer nombre ||``.

Choisis un visage triste.

```blocks

basic.forever(function () {
    if (Math.round(pins.analogReadPin(AnalogPin.P0)) > 0) {
        basic.showNumber(pins.analogReadPin(AnalogPin.P1))
        basic.showIcon(IconNames.Sad)
    } else {
    	
    }
})

```

## Étape 22

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| basic: montrer l'icône ||``.

```blocks

basic.forever(function () {
    if (Math.round(pins.analogReadPin(AnalogPin.P0)) > 0) {
        basic.showNumber(pins.analogReadPin(AnalogPin.P1))
        basic.showIcon(IconNames.Sad)
        pins.digitalWritePin(DigitalPin.P0, 0)
    } else {
    	
    }
})

```

## Étape 23

Modifie la valeur ``|| pins: P0 ||`` du bloc ``|| pins: écrire sur la broche ||`` par ``|| pins: P2 ||``.

Modifie la valeur ``|| pins: 0 ||`` du bloc ``|| pins: écrire sur la broche ||`` par ``|| pins: 1 ||``.

```blocks

basic.forever(function () {
    if (Math.round(pins.analogReadPin(AnalogPin.P0)) > 0) {
        basic.showNumber(pins.analogReadPin(AnalogPin.P1))
        basic.showIcon(IconNames.Sad)
        pins.digitalWritePin(DigitalPin.P2, 1)
    } else {
    	
    }
})

```

## Étape 24

Ajoute le bloc ``|| basic: montrer nombre ||`` dans le bloc ``|| logic: sinon ||``.

```blocks

basic.forever(function () {
    if (Math.round(pins.analogReadPin(AnalogPin.P0)) > 0) {
        basic.showNumber(pins.analogReadPin(AnalogPin.P1))
        basic.showIcon(IconNames.Sad)
        pins.digitalWritePin(DigitalPin.P2, 1)
    } else {
        basic.showNumber(0)
    }
})

```

## Étape 25

Remplace la valeur ``|| basic: 0 ||`` du bloc ``|| basic: montrer nombre ||`` par le bloc ``|| pins: lire la broche analogique ||``.

```blocks

basic.forever(function () {
    if (Math.round(pins.analogReadPin(AnalogPin.P0)) > 0) {
        basic.showNumber(pins.analogReadPin(AnalogPin.P1))
        basic.showIcon(IconNames.Sad)
        pins.digitalWritePin(DigitalPin.P2, 1)
    } else {
        basic.showNumber(pins.analogReadPin(AnalogPin.P0))
    }
})


```

## Étape 26

Modifie la valeur ``|| pins: P0 ||`` du bloc ``|| pins: lire la broche analogique ||`` par ``|| pins: P1 ||``.

```blocks

basic.forever(function () {
    if (Math.round(pins.analogReadPin(AnalogPin.P0)) > 0) {
        basic.showNumber(pins.analogReadPin(AnalogPin.P1))
        basic.showIcon(IconNames.Sad)
        pins.digitalWritePin(DigitalPin.P2, 1)
    } else {
        basic.showNumber(pins.analogReadPin(AnalogPin.P1))
    }
})

```


## Étape 27

Ajoute le bloc ``|| basic: montrer l'icône ||`` sous le bloc ``|| basic: montrer nombre ||``.

Choisis un visage souriant.

```blocks

basic.forever(function () {
    if (Math.round(pins.analogReadPin(AnalogPin.P0)) > 0) {
        basic.showNumber(pins.analogReadPin(AnalogPin.P1))
        basic.showIcon(IconNames.Sad)
        pins.digitalWritePin(DigitalPin.P2, 1)
    } else {
        basic.showNumber(pins.analogReadPin(AnalogPin.P0))
        basic.showIcon(IconNames.Happy)
    }
})

```

## Étape 28

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| basic: montrer l'icône ||``.

```blocks

basic.forever(function () {
    if (Math.round(pins.analogReadPin(AnalogPin.P0)) > 0) {
        basic.showNumber(pins.analogReadPin(AnalogPin.P1))
        basic.showIcon(IconNames.Sad)
        pins.digitalWritePin(DigitalPin.P2, 1)
    } else {
        basic.showNumber(pins.analogReadPin(AnalogPin.P0))
        basic.showIcon(IconNames.Happy)
        pins.digitalWritePin(DigitalPin.P0, 0)
    }
})

```

## Étape 29

Modifie la valeur ``|| pins: P0 ||`` du bloc ``|| pins: écrire sur la broche ||`` par ``|| pins: P2 ||``.

La valeur ``|| pins: 0 ||`` du bloc ``|| pins: écrire sur la broche ||`` demeure la même.

```blocks

basic.forever(function () {
    if (Math.round(pins.analogReadPin(AnalogPin.P0)) > 0) {
        basic.showNumber(pins.analogReadPin(AnalogPin.P1))
        basic.showIcon(IconNames.Sad)
        pins.digitalWritePin(DigitalPin.P2, 1)
    } else {
        basic.showNumber(pins.analogReadPin(AnalogPin.P0))
        basic.showIcon(IconNames.Happy)
        pins.digitalWritePin(DigitalPin.P2, 0)
    }
})

```

## @showdialog

Bravo tu as terminé la programmation du système d'arrosage automatisé.

Teste le programme.