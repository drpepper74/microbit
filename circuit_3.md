# Circuits électriques

# Tutoriel 3

## @showdialog

Programme le micro:bit pour qu'une lumière LED s'allume s'il est secoué.

## Étape 1

Supprime les blocs ``||basic:au démarrage||`` et ``||basic:toujours||``.

## Étape 2

Ajoute le bloc ``|| pins: écrire sur la broche ||`` dans le bloc ``|| input: lorsque secouer ||``.


```blocks

input.onGesture(Gesture.Shake, function () {
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 3

Modifie les valeurs du bloc ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P2 ||``.

Remplace la valeur ``|| pins: 0 ||`` par ``|| pins: 1 ||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    pins.digitalWritePin(DigitalPin.P2, 1)
})

```

## Étape 4

Ajoute le bloc ``|| basic: pause (ms) ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Modifie la valeur du bloc ``|| basic: pause (ms) ||``.

Remplace la valeur ``|| basic: 100 ||`` par ``|| basic: 500 ||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    pins.digitalWritePin(DigitalPin.P2, 1)
    basic.pause(500)
})

```

## Étape 5

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| basic: pause (ms) ||``.


Modifie les valeurs du bloc ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P2 ||``.


```blocks

input.onGesture(Gesture.Shake, function () {
    pins.digitalWritePin(DigitalPin.P2, 1)
    basic.pause(500)
    pins.digitalWritePin(DigitalPin.P2, 0)
})


```

## Étape 6

Ajoute le bloc ``|| loops: répéter ||`` dans le bloc ``|| input: lorsque secouer ||``.

Modifie la valeur du bloc ``|| loops: répéter ||``.

Remplace la valeur ``|| loops: 4 ||`` par ``|| loops: 10 ||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    for (let index = 0; index < 10; index++) {
        pins.digitalWritePin(DigitalPin.P2, 1)
        basic.pause(500)
        pins.digitalWritePin(DigitalPin.P2, 0)
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