# Circuits électriques - Tutoriel 1

## @showdialog

Programme le micro:bit pour qu'il allume une lumière LED.

## Étape 1

Supprime le bloc ``||basic:au démarrage||``.

## Étape 2

Ajoute le bloc ``|| pins: écrire sur la broche ||`` dans le bloc ``||basic: toujours||``.

```blocks

basic.forever(function () {
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 3

Modifie les valeurs du bloc ``|| pins: écrire sur la broche ||``.

La valeur ``|| pins: P0 ||`` demeure la même.

Remplace la valeur ``|| pins: 0 ||`` par 1.

```blocks

basic.forever(function () {
    pins.digitalWritePin(DigitalPin.P0, 1)
})

```

## Étape 4

Ajoute le bloc ``||basic: pause||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``||basic: 100||`` par ``||basic: pause (ms) 500||``.

```blocks

basic.forever(function () {
    pins.digitalWritePin(DigitalPin.P0, 1)
    basic.pause(500)
})

```

## Étape 5

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``||basic: pause||``.

Les valeurs du bloc ``|| pins: écrire sur la broche ||`` demeurent les mêmes.

```blocks

basic.forever(function () {
    pins.digitalWritePin(DigitalPin.P0, 1)
    basic.pause(500)
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 6

Ajoute le bloc ``||basic: pause||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``||basic: 100||`` par ``||basic: pause (ms) 500||``.

```blocks

basic.forever(function () {
    pins.digitalWritePin(DigitalPin.P0, 1)
    basic.pause(500)
    pins.digitalWritePin(DigitalPin.P0, 0)
    basic.pause(500)
})

```

# @showdialog 

Réalise le branchement ci-dessous.

![MicroSeb](https://github.com/sbergeroncp/micro-seb/blob/master/1.png?raw=true)

## @showdialog 

Félicitations! Tu as terminé de programmer un circuit électrique avec une lumière LED.

Pour tester le circuit électrique, télécharge la programmation dans le micro:bit.