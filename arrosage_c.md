# Système d'arrosage automatisé

## @showdialog
Programme les différentes composants du système d'arrosage automatisé.

## Étape 1

Supprime le bloc ``||basic:toujours||``.

## Étape 2

Ajoute le bloc ``|| pins: écrire sur la broche ||`` dans le bloc ``||basic: au démarrage||``.

```blocks

pins.digitalWritePin(DigitalPin.P0, 0)

```
## Étape 3

Modifie la valeur ``|| pins: P0 ||`` du bloc ``|| pins: écrire sur la broche ||`` par ``|| pins: P2 ||``.

La valeur  ``|| pins: 0 ||`` du bloc ``|| pins: écrire sur la broche ||`` demeure la même.

```blocks

pins.digitalWritePin(DigitalPin.P2, 0)

```

## Étape 4

Ajoute le bloc ``|| input: lorsque le bouton A est pressé. ||`` dans la zone de programmation.

Ajoute le bloc ``|| basic: montrer nombre ||`` dans le bloc ``|| input: lorsque le bouton A est pressé. ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    basic.showNumber(0)
})

```

## Étape 5

Modifie la valeur ``|| basic: 0 ||`` du bloc ``|| basic: montrer nombre ||`` par le bloc ``|| math: arrondi ||``

```blocks

input.onButtonPressed(Button.A, function () {
    basic.showNumber(Math.round(0))
})

```

## Étape 6

Modifie la valeur ``|| math: 0 ||`` du bloc ``|| math: arrondi ||`` par le bloc ``|| pins: lire la broche analogique ||``

```blocks

input.onButtonPressed(Button.A, function () {
    basic.showNumber(Math.round(pins.analogReadPin(AnalogPin.P0)))
})

```

## Étape 7

Modifie la valeur ``|| pins: P0 ||`` du bloc ``|| pins: lire la broche analogique ||`` par ``|| pins: P1 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    basic.showNumber(Math.round(pins.analogReadPin(AnalogPin.P1)))
})

```

## Étape 8

Ajoute le bloc ``|| input: lorsque le bouton B est pressé. ||``.

Ajoute le bloc ``|| pins: écrire sur la broche ||`` dans le bloc ``|| input: lorsque le bouton B est pressé. ||``.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 9

Modifie la valeur ``|| pins: P0 ||`` du bloc ``|| pins: écrire sur la broche ||`` par ``|| pins: P2 ||``.

Modifie la valeur ``|| pins: 0 ||`` du bloc ``|| pins: écrire sur la broche ||`` par ``|| pins: 1 ||``.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.digitalWritePin(DigitalPin.P2, 1)
})

```

## Étape 10

Ajoute le bloc ``|| basic: pause (ms) ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Modifie la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||`` par ``|| basic: 30000 ||``.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.digitalWritePin(DigitalPin.P2, 1)
    basic.pause(30000)
})

```

## Étape 11

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| basic: pause (ms) 30000. ||``.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.digitalWritePin(DigitalPin.P2, 1)
    basic.pause(1000)
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 12

Modifie la valeur ``|| pins: P0 ||`` du bloc ``|| pins: écrire sur la broche ||`` par ``|| pins: P2 ||``.

La valeur ``|| pins: 0 ||`` du bloc ``|| pins: écrire sur la broche ||`` demeure la même.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.digitalWritePin(DigitalPin.P2, 1)
    basic.pause(1000)
    pins.digitalWritePin(DigitalPin.P2, 0)
})

```

## Étape 13

Ajoute le bloc ``|| loops: chaque (ms) ||`` dans la zone de programmation.

Modifie la valeur ``|| loops: 500 ||`` du bloc ``|| loops: chaque (ms) ||`` par ``|| loops: 60000 ||``.

```blocks

loops.everyInterval(60000, function () {
	
})

```

## Étape 14

Ajoute le bloc ``|| logic: si vrai alors sinon ||`` dans le bloc ``|| loops: chaque (ms) ||``.

```blocks

loops.everyInterval(60000, function () {
	
})

```

## Étape 15

Remplace la valeur ``|| logic: vrai ||`` du bloc ``|| logic: si vrai alors ||`` par le bloc ``|| logic: 0 < 0 ||``.

Remplace la valeur ``||logic: < ||`` du bloc ``|| logic: 0 < 0 ||`` par la valeur ``|| logic: > ||``.

```blocks

loops.everyInterval(60000, function () {
    if (0 > 0) {
    	
    } else {
    	
    }
})

```

## Étape 16

Remplace la valeur ``|| logic: 0 ||`` de gauche du bloc ``|| logic: 0 > 0 ||`` par le bloc ``|| math: arrondi ||``.

```blocks

loops.everyInterval(60000, function () {
    if (Math.round(0) > 0) {
    	
    } else {
    	
    }
})

```

## Étape 17

Remplace la valeur ``|| math: 0 ||``  du bloc ``|| math: arrondi ||`` par le bloc ``|| pins: lire la broche analogique ||``.

```blocks

loops.everyInterval(60000, function () {
    if (Math.round(pins.analogReadPin(AnalogPin.P0)) > 0) {
    	
    } else {
    	
    }
})

```

## Étape 17

Modifie la valeur ``|| pins: P0 ||``  du bloc ``|| pins: lire la broche ||`` par ``|| pins: P1 ||``.

```blocks

loops.everyInterval(60000, function () {
    if (Math.round(pins.analogReadPin(AnalogPin.P1)) > 0) {
    	
    } else {
    	
    }
})

```

## Étape 18

Modifie la valeur ``|| logic: 0 ||`` de droite du bloc ``|| logic: si vrai alors ||`` par ``|| logic: 600 ||``.

```blocks

loops.everyInterval(60000, function () {
    if (Math.round(pins.analogReadPin(AnalogPin.P1)) > 600) {
    	
    } else {
    	
    }
})

```

## Étape 19

Ajoute le bloc ``|| pins: écrire sur la broche ||`` dans le le bloc ``|| logic: si vrai alors ||``.

```blocks

loops.everyInterval(60000, function () {
    if (Math.round(pins.analogReadPin(AnalogPin.P1)) > 600) {
        pins.digitalWritePin(DigitalPin.P0, 0)
    } else {
    	
    }
})

```

## Étape 20

Modifie la valeur ``|| pins: P0 ||`` du bloc ``|| pins: écrire sur la broche ||`` par ``|| pins: P2 ||``.

Modifie la valeur ``|| pins: 0 ||`` du bloc ``|| pins: écrire sur la broche ||`` par ``|| pins: 1 ||``.

```blocks

loops.everyInterval(60000, function () {
    if (Math.round(pins.analogReadPin(AnalogPin.P1)) > 600) {
        pins.digitalWritePin(DigitalPin.P2, 1)
    } else {
    	
    }
})

```

## Étape 21

Ajoute le bloc ``|| basic: pause (ms) ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Modifie la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||`` par ``|| basic: 30000 ||``.

```blocks

loops.everyInterval(60000, function () {
    if (Math.round(pins.analogReadPin(AnalogPin.P1)) > 600) {
        pins.digitalWritePin(DigitalPin.P2, 1)
        basic.pause(30000)
    } else {
    	
    }
})

```

## Étape 22

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| basic: pause (ms) 30000. ||``.

```blocks

loops.everyInterval(60000, function () {
    if (Math.round(pins.analogReadPin(AnalogPin.P1)) > 600) {
        pins.digitalWritePin(DigitalPin.P2, 1)
        basic.pause(30000)
        pins.digitalWritePin(DigitalPin.P0, 0)
    } else {
    	
    }
})

```

## Étape 23

Modifie la valeur ``|| pins: P0 ||`` du bloc ``|| pins: écrire sur la broche ||`` par ``|| pins: P2 ||``.

La valeur ``|| pins: 0 ||`` du bloc ``|| pins: écrire sur la broche ||`` demeure la même.

```blocks

loops.everyInterval(60000, function () {
    if (Math.round(pins.analogReadPin(AnalogPin.P1)) > 600) {
        pins.digitalWritePin(DigitalPin.P2, 1)
        basic.pause(30000)
        pins.digitalWritePin(DigitalPin.P2, 0)
    } else {
    	
    }
})


```

## Étape 24

Ajoute le bloc ``|| basic: montrer l'cône ||`` dans le bloc ``|| logic: sinon. ||``.

Regarde l'indice! :)

```blocks

loops.everyInterval(60000, function () {
    if (Math.round(pins.analogReadPin(AnalogPin.P1)) > 600) {
        pins.digitalWritePin(DigitalPin.P2, 1)
        basic.pause(30000)
        pins.digitalWritePin(DigitalPin.P2, 0)
    } else {
        basic.showIcon(IconNames.Heart)
    }
})

```

## @showdialog

Bravo tu as terminé la programmation du système d'arrosage automatisé.

Teste le programme.