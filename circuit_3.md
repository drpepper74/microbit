# Circuits électriques - Tutoriel 3

## @showdialog

Programme le micro:bit et le circuit électrique.

## Étape 1

Ajoute le bloc ``|| pins: écrire sur la broche ||`` dans le bloc ``|| input: lorsque secouer ||``.


```blocks

input.onGesture(Gesture.Shake, function () {
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 2

Modifie les valeurs du bloc ``|| pins: écrire sur la broche ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P2 ||``.

Remplace la valeur ``|| pins: 0 ||`` par ``|| pins: 1 ||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    pins.digitalWritePin(DigitalPin.P2, 1)
})

```

## Étape 3

Ajoute le bloc ``|| basic: pause ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Modifie la valeur du bloc ``|| basic: pause ||``.

Remplace la valeur ``|| basic: 100 ||`` par ``|| basic: 500 ||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    pins.digitalWritePin(DigitalPin.P2, 1)
    basic.pause(500)
})

```

## Étape 4

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| basic: pause (ms) ||``.

Modifie les valeurs du bloc ``|| pins: écrire sur la broche ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P2 ||``.

La valeur ``|| pins: 0 ||`` demeure la même.


```blocks

input.onGesture(Gesture.Shake, function () {
    pins.digitalWritePin(DigitalPin.P2, 1)
    basic.pause(500)
    pins.digitalWritePin(DigitalPin.P2, 0)
})


```

## Étape 5

Ajoute le bloc ``|| basic: pause ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Modifie la valeur du bloc ``|| basic: pause ||``.

Remplace la valeur ``|| basic: 100 ||`` par ``|| basic: 500 ||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    pins.digitalWritePin(DigitalPin.P2, 1)
    basic.pause(500)
    pins.digitalWritePin(DigitalPin.P2, 0)
    basic.pause(500)
})

```

## Étape 6

Ajoute le bloc ``|| loops: répéter ||`` dans le bloc ``|| input: lorsque secouer ||``.

Insère la séquence de programmation dans celui-ci.

Modifie la valeur du bloc ``|| loops: répéter ||``.

Remplace la valeur ``|| loops: 4 ||`` par ``|| loops: 5 ||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    for (let index = 0; index < 5; index++) {
        pins.digitalWritePin(DigitalPin.P2, 1)
        basic.pause(500)
        pins.digitalWritePin(DigitalPin.P2, 0)
        basic.pause(500)
    }
})

```

## @showdialog 

Réalise le branchement ci-dessous.

La couleur des fils n'a pas d'importance!

![MicroSeb](https://github.com/sbergeroncp/micro-seb/blob/master/3.png?raw=true)

## @showdialog 

Félicitations! Tu as terminé de programmer un circuit électrique avec une lumière LED.

Pour tester le circuit électrique, télécharge la programmation dans le micro:bit.