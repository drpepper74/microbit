# Système d'arrosage automatisé

## @showdialog
Programme le système d'arrosage automatisé de la classe.

## Étape 1

Supprime le bloc ``||basic: toujours||``.


## Étape 2

Ajoute le bloc ``|| pins: écrire sur la broche ||`` dans le bloc ``||basic: au démarrage||``.

```blocks

pins.digitalWritePin(DigitalPin.P0, 0)

```
## Étape 3

Remplace la valeur ``|| pins: P0 ||`` du bloc ``|| pins: écrire sur la broche ||`` par ``|| pins: P1 ||``.

La valeur  ``|| pins: 0 ||`` du bloc ``|| pins: écrire sur la broche ||`` demeure la même.

```blocks

pins.digitalWritePin(DigitalPin.P1, 0)

```

## Étape 4

Ajoute le bloc ``|| pins: écrire sur la broche ||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 5

Remplace la valeur ``|| pins: P0 ||`` du bloc ``|| pins: écrire sur la broche ||`` par ``|| pins: P1 ||``.

Remplace la valeur  ``|| pins: 0 ||`` du bloc ``|| pins: écrire sur la broche ||`` par ``|| pins: 1 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.digitalWritePin(DigitalPin.P1, 1)
})

```

## Étape 6

Ajoute le bloc ``|| pins: écrire sur la broche ||`` dans le bloc ``||input: lorsque le bouton B est pressé||``.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 7

Remplace la valeur ``|| pins: P0 ||`` du bloc ``|| pins: écrire sur la broche ||`` par ``|| pins: P1 ||``.

La valeur  ``|| pins: 0 ||`` du bloc ``|| pins: écrire sur la broche ||`` demeure la même.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.digitalWritePin(DigitalPin.P1, 0)
})

```

## Étape 8

Ajoute le bloc ``|| loops: chaque ms ||``.

Remplace la valeur ``|| loops: 500 ||`` du bloc ``|| loops: chaque ms ||`` par le bloc ``|| math: 0 x 0 ||``.

```blocks

loops.everyInterval(0 * 0, function () {
	
})

```


## Étape 9

Modifie le bloc ``|| math: 0 x 0 ||``.

Remplace la valeur ``|| math:  0 ||`` de gauche par le bloc ``|| math: 0 x 0 ||``.

Remplace la valeur ``|| math:  0 ||`` de droite par le bloc ``|| math: 0 x 0 ||``.

```blocks

loops.everyInterval(0 * 0 * (0 * 0), function () {
	
})

```
## Étape 10

Modifie les bloc ``|| math: 0 x 0 ||``.

Remplace les valeurs ``|| math:  0 ||`` par ``|| math:  1000 ||``, ``|| math:  60 ||``, ``|| math:  60 ||`` et ``|| math:  12 ||``.

Autrement dit, la pompe submergée sera activée toutes les 12 heures.

```blocks

loops.everyInterval(1000 * 60 * (60 * 12), function () {
	
})

```

## Étape 11

Ajoute le bloc ``|| pins: écrire sur la broche ||`` dans le bloc ``||loops: chaque ms||``.

```blocks

loops.everyInterval(1000 * 60 * (60 * 12), function () {
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 12

Remplace la valeur ``|| pins: P0 ||`` du bloc ``|| pins: écrire sur la broche ||`` par ``|| pins: P1 ||``.

Remplace la valeur  ``|| pins: 0 ||`` du bloc ``|| pins: écrire sur la broche ||`` par ``|| pins: 1 ||``.

```blocks

loops.everyInterval(1000 * 60 * (60 * 12), function () {
    pins.digitalWritePin(DigitalPin.P1, 1)
})

```

## Étape 13

Ajoute le bloc ``|| basic: pause (ms) 100||`` sous le bloc ``|| pins: écrire sur la broche ||``.

```blocks

loops.everyInterval(1000 * 60 * (60 * 12), function () {
    pins.digitalWritePin(DigitalPin.P1, 1)
    basic.pause(100)
})

```

## Étape 14


Remplace la valeur ``|| basic: 100 ||`` par le bloc ``|| math: 0 x 0 ||``.

```blocks

loops.everyInterval(1000 * 60 * (60 * 12), function () {
    pins.digitalWritePin(DigitalPin.P1, 1)
    basic.pause(0 * 0)
})

```

## Étape 15

Modifie le bloc ``|| math: 0 x 0 ||``.

Remplace la valeur ``|| math: 0 ||`` de gauche par la valeur ``|| math: 1000 ||``.

Remplace la valeur ``|| math: 0 ||`` de droite par la valeur ``|| math: 20 ||``.

Autrement dit, la popme submergée sera actionnée pendant 20 secondes.

```blocks

loops.everyInterval(1000 * 60 * (60 * 12), function () {
    pins.digitalWritePin(DigitalPin.P1, 1)
    basic.pause(1000 * 12)
})

```

## Étape 16

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``||basic: pause (ms)||``.

```blocks

loops.everyInterval(1000 * 60 * (60 * 12), function () {
    pins.digitalWritePin(DigitalPin.P1, 1)
    basic.pause(1000 * 12)
    pins.digitalWritePin(DigitalPin.P0, 0)
})


```

## Étape 17

Remplace la valeur ``|| pins: P0 ||`` du bloc ``|| pins: écrire sur la broche ||`` par ``|| pins: P1 ||``.

La valeur  ``|| pins: 0 ||`` du bloc ``|| pins: écrire sur la broche ||`` demeure la même.

```blocks

loops.everyInterval(1000 * 60 * (60 * 12), function () {
    pins.digitalWritePin(DigitalPin.P1, 1)
    basic.pause(1000 * 12)
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## @showdialog

Bravo tu as terminé la programmation du système d'arrosage automatisé.

Télécharge et teste le programme.